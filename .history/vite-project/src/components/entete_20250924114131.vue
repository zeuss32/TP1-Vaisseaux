<template>
	<nav class="navbar navbar-expand-lg bg-dark fixed-top text-danger ">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">TP-VUEJS</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="SousSections/systemes.vue">SYSTÈMES</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">VAISSEAUX</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            BIENS
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">X: {{ x }}</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Y: {{ y }}</a></li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</nav>

	<div class="container-fluid w-100">
		<div id="header_carousel" class="carousel slide" data-bs-ride="carousel">
			<div class="carousel-inner">
				<div class="carousel-item active">
					<img
						src="../../images/rocket-ship-space-background/5937322.jpg"
						class="d-block w-100"
						alt="..."
					/>
				</div>
				<div class="carousel-item">
					<img
						src="../../images/realistic-rocket-launch-composition-with-spacecraft-flying-clouds-vector-illustration/2204.q703.029.F.m004.c7.rocket spacecraft lounch realistic.jpg"
						class="d-block w-100"
						alt="..."
					/>
				</div>
				<div class="carousel-item">
					<img
						src="../../images/rocket-launch-realistic-background-with-spacecraft-flying-into-space-earth-vector-illustration/2111.q703.017.F.m004.c7.rocket spacecraft realistic.jpg"
						class="d-block w-100"
						alt="..."
					/>
				</div>
			</div>
		</div>

		<h1 class="text-center bg-primary text-white titrePage">
			Starship Company🚀
		</h1>
		<h2>coordonnées:({{ x }},{{ y }})</h2>
	</div>
	<CorpsDePage @nouvellesCoordonnees="newCoords" />
</template>

<script setup>
import { ref } from "vue";
import CorpsDePage from "./CorpsDePage.vue";

let x = ref(0);
let y = ref(0);
function newCoords(newX, newY) {
	x.value = newX;
	y.value = newY;
}
</script>

<style>
.titrePage {
	color: white !important;
}
</style>
