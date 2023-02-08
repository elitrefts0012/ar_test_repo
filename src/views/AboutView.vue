<!-- Import the component -->
<!--<script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>-->

<!-- Use it like any other HTML element -->

<template>
  <div class="about">
    <h1>This is an about page</h1>
<!--    <model-viewer alt="Neil Armstrong's Spacesuit from the Smithsonian Digitization Programs Office and National Air and Space Museum" src="shared-assets/models/NeilArmstrong.glb" ar environment-image="shared-assets/environments/moon_1k.hdr" poster="shared-assets/models/NeilArmstrong.webp" shadow-intensity="1" camera-controls touch-action="pan-y" generate-schema></model-viewer>-->
  </div>
</template>

<script>
import { Scene, WebGLRenderer } from 'three';
import { ARUtils, ARPerspectiveCamera, ARView } from 'three.ar.js';

async function init() {
  const display = await ARUtils.getARDisplay();
  const renderer = new WebGLRenderer({ alpha: true });
  const arView = new ARView(display, renderer);

  // And so forth...
}
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
