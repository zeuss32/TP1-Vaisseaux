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
                @click="$emit('nouvellesCoordonnees', sysP.x, sysP.y)"
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

defineProps({
  systems: Object,
});

const emit = defineEmits(["nouvellesCoordonnees"]);


</script>

<style scoped>
</style>
