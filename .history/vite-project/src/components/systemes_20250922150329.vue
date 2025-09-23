<template>
	<div class="container-fluid">
		<div class="card" style="width: 18rem">
			<div class="card-header">Système:{{ Systemes.name }}</div>
			<div class="card-body">
				<p class="card-title">Symbole:{{ Systemes.symbol }}</p>
				<p class="card-text">Planètes:{{ Systemes.planets.length }}</p>
			</div>
		</div>
	</div>
</template>

<script setup>
defineProps({
	Systemes: Object,
});
console.log("Systemes reçu:", props.Systemes);
</script>

<style></style>
