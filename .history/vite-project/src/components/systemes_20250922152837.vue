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
			</div>
		</div>
	</div>
</template>

<script setup>
const props = defineProps({
	Systemes: Object,
});
</script>

<style></style>
