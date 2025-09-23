<template>
	<div class="container-fluid">
		<div class="card" style="width: 18rem">
			<div class="card-header">Système:{{ Systemes.systems.name }}</div>
			<div class="card-body">
				<p class="card-title">Symbole:{{ Systemes.systems.symbol }}</p>
				<p class="card-text">Planètes:{{ Systemes.systems.planets.length }}</p>
			</div>
		</div>
	</div>
</template>

<script setup>
difineProps({
	Systemes: Object,
});
</script>

<style></style>
