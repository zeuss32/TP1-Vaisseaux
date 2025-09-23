<template>
	<div class="container-fluid">
		<div class="card" style="width: 18rem">
			<div class="card-header">
				Système: <strong>{{ Systemes.name }}</strong>
			</div>
			<div class="card-body">
				<p class="card-title">
					Symbole: <strong>{{ Systemes.symbol }}</strong>
				</p>
				<p class="card-text">
					Planètes: <strong>{{ Systemes.planets.length }}</strong>
                   
                            <div v-for="planets in Systemes.planets" :key="symbol" class="card-text">
                            <ul class="list-group list-group-flush">
                                <li class="list-group-item">nom :{{planets.symbol  }}</li>
                                <li class="list-group-item">Symbole planete{{planets.symbol  }}</li>

                            </ul>
                            <button
                                class="btn btn-success"
                                @click="$emit('nouvellesCoordonnees', planets.x, planets.y)"
                            >
                                Position Actuelle
                            </button>
                        </div>
                   
				</p>
				
			</div>
		</div>
	</div>
</template>

<script setup>
import Entete from "./entete.vue";

const props = defineProps({
	Systemes: Object,
});
const emit = defineEmits(["nouvellesCoordonnees"]);
</script>

<style></style>
