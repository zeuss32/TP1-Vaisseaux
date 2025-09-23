<template>
	<div class="container-fluid">
		<h1>Systemes Spaciaux</h1>
		<div class="row">
			<div class="col-md-4" v-for="Sys in systemesJson.systems" :key="Sys.name">
				<Systemes :Systemes="Sys" />
			</div>
		</div>
	</div>
</template>

<script setup>
import Systemes from "./Systemes.vue";
import vaisseaux from "./vaisseaux.vue";
import biensEtMateriaux from "./biensEtMateriaux.vue";
import biensJson from "../data/biens.json";
import systemesJson from "../data/systemes.json";
import vaisseauxJson from "../data/vaisseaux.json";
</script>

<style></style>
