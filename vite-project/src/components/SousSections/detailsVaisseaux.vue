<template>
  <div
    class="modal fade"
    :id="information.name"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">Information</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <h5 class="modal-body">Nom : {{ information.name }}</h5>
        <h5 class="modal-body">Classe : {{ information.class }}</h5>
        <h5 class="modal-body">
          Manifacturier : {{ information.manufacturer }}
        </h5>
        <h5 class="modal-body">Type : {{ information.type }}</h5>
        <h5 class="modal-body">
          Capacité du cargo : {{ information["maximum cargo"] }}
        </h5>
        <h5 class="modal-body">Blindage : {{ information.plating }}</h5>
        <h5 class="modal-body">Vitesse : {{ information.speed }}</h5>
        <h5 class="modal-body">Nombre d'armes : {{ information.weapons }}</h5>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
defineProps({
  information: Object,
  index: Number,
});
</script>
