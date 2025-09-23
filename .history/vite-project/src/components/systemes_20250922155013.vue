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
				</p>
				<a
					href="#"
					class="btn btn-success"
					@click="nouvellesCoordonnees(Systemes.planets.x, Systemes.planets.y)"
				>
					Position Actuelle</a
				>
			</div>
		</div>
	</div>
</template>

<script setup>
import Entete from "./entete.vue";

const props = defineProps({
	Systemes: Object,
});
function nouvellesCoordonnees(x, y) {
	Entete.x = x;
	Entete.y = y;
}
</script>

<style></style>
