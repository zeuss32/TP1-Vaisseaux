<template>
  <div class="row">
    <div class="col-sm-2" v-for="(ship, index) in vaisseau">
      <div class="card bg-info">
        <h5 class="card-title">{{ ship.name }}</h5>
        <h5 class="card-title">Manufacturier : {{ ship.manufacturer }}</h5>
        <h5 class="card-title">Class : {{ ship.class }}</h5>
        <h5 class="card-title">
          Capacité du cargo : {{ ship["maximum cargo"] }}
        </h5>

        <button
          type="button"
          class="btn btn-primary"
          data-bs-toggle="modal"
          :data-bs-target="combinaison(ship.name)"
        >
          Voir les détails
        </button>

        <DetailsVaisseau :information="ship" :index="index"></DetailsVaisseau>
      </div>
      <br />
    </div>
  </div>
</template>

<script setup>
import DetailsVaisseau from "@/components/SousSections/detailsVaisseaux.vue";
defineProps({
  vaisseau: Array,
});

function combinaison(index) {
  return "#" + index;
}
</script>

<style scoped>
</style>
