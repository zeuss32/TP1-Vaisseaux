<template>
  <div class="container">
    <div class="row" v-for="sys in systems">
      <div class="card col-sm-12">
        <br />
        <h5 class="card-title">Système : {{ sys.name }}</h5>
        <h5 class="card-title">Symbôle : {{ sys.symbol }}</h5>
        <h5 class="card-title">Nbre de planètes : {{ sys.planets.length }}</h5>
        <br />
        <div class="row">
          <div class="col-sm-2" v-for="sysP in sys.planets">
            <div class="card bg-success">
              <h5 class="card-title">{{ sysP.name }}</h5>
              <h5 class="card-title">{{ sysP.symbol }}</h5>
              <h5 class="card-title">Type: {{ sysP.type }}</h5>
              <button
                @click="changementCoordonnee(sysP)"
                :disabled="
                  ancienneCoordonne.x == sysP.x && ancienneCoordonne.y == sysP.y
                "
                class="btn btn-danger"
              >
                Localisation
              </button>
            </div>
            <br />
          </div>
        </div>
      </div>
      <br />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { defineEmits } from "vue";
defineProps({
  systems: Array,
  x: Number,
  y: Number,
});

const ancienneCoordonne = ref({});
const emit = defineEmits(["nouvellesCoordonnees"]);

const changementCoordonnee = (coord) => {
  ancienneCoordonne.value.x = coord.x;
  ancienneCoordonne.value.y = coord.y;
  emit("nouvellesCoordonnees", coord.x, coord.y);
};
</script>

<style scoped>
</style>
