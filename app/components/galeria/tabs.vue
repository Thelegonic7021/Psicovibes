<script setup lang="ts">
import Grid from './grid.vue';


</script>

<template>
    <ul class="nav nav-pills mb-3" id="pills-tab" role="tablist">
        <li class="nav-item" role="presentation">
            <button class="nav-link active" id="pills-sectores-tab" data-bs-toggle="pill" data-bs-target="#pills-sectores" type="button" role="tab" aria-controls="pills-sectores" aria-selected="true">Sectores</button>
        </li>
        <li class="nav-item" role="presentation">
            <button class="nav-link" id="pills-profile-tab" data-bs-toggle="pill" data-bs-target="#pills-profile" type="button" role="tab" aria-controls="pills-profile" aria-selected="false">Dias especiales</button>
        </li>
        <li class="nav-item" role="presentation">
            <button class="nav-link" id="pills-contact-tab" data-bs-toggle="pill" data-bs-target="#pills-contact" type="button" role="tab" aria-controls="pills-contact" aria-selected="false">Mensajes</button>
        </li>
    </ul>
    <div class="tab-content" id="pills-tabContent">
        <div class="tab-pane fade show active" id="pills-sectores" role="tabpanel" aria-labelledby="pills-sectores-tab"><Grid :direcciones="['/Galeria/SectorAsesoria.jpg', '/Galeria/SectorColectivos.jpg', '/Galeria/SectorEducativo.jpg','/Galeria/SectorEmpresarial.jpg']" :numRows="2" :numCols="2"/></div>
        <div class="tab-pane fade" id="pills-profile" role="tabpanel" aria-labelledby="pills-profile-tab">...</div>
        <div class="tab-pane fade" id="pills-contact" role="tabpanel" aria-labelledby="pills-contact-tab">...</div>
    </div>
</template>