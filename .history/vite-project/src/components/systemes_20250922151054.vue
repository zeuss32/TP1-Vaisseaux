<template>
	<div class="container-fluid">
		<div
			class="card"
			v-for="sys in Systemes"
			:key="sys.name"
			style="width: 18rem"
		>
			<div class="card-header">Système:{{ Sys.name }}</div>
			<div class="card-body">
				<p class="card-title">Symbole:{{ Sys.symbol }}</p>
				<p class="card-text">Planètes:{{ Sys.planets.length }}</p>
			</div>
		</div>
	</div>
</template>

<script setup>
defineProps({
	Systemes: Array,
});
console.log("Systemes reçu:", props.Systemes);
</script>

<style></style>
