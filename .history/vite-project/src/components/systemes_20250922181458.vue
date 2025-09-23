<template>
	<div class="container-fluid">
        <div class="row">
		<div class="card " >
			<div class="card-title bg-primary h3">
				Système: <strong>{{ Systemes.name }}</strong>
			</div>
			<div class="card-body bg-primary">
				<p class="card-text">
					Symbole: <strong>{{ Systemes.symbol }}</strong>
				</p>
				<p class="card-text">
					Planètes: <strong>{{ Systemes.planets.length }}</strong>
                   
                            <div v-for="planet in Systemes.planets" :key="planet.symbol" class="card bg-outline-dark ">
                            <ul class="list-group list-group-flush ">
                                <li class="list-group-item texte ">nom :{{planet.name  }}</li>
                                <li class="list-group-item">Symbole: {{planet.symbol  }}</li>
                                <li class="list-group-item">type : {{planet.type  }}</li>
                                <li
                                class="btn btn-success"
                                @click="$emit('nouvellesCoordonnees', planet.x, planet.y)"
                            >
                                Position Actuelle
                            </li>
                            </ul>
                            
                        </div>
                   
				</p>
				
			</div>
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
