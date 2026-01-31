
<script setup lang="ts">
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const images = Array.from({length: 3}, (_, index)=> ({
    id:index + 1,
    url: `/Array/${index+1}.png`
}))

const config = {
    height: 700,
    itemsToShow: 1,
    gap: 25,
    wrapAround: true,
}
</script>

<template>
    <div>
        <div class="contenedor-carrusel">
            <div>
                <Carousel v-bind="config" >
                    <Slide v-for="image in images" :key="image.id">
                        <img :src="image.url" alt="" style="width: 100%; height: 100%; object-fit: cover;">
                    </Slide>

                    <template #addons>
                        <Navigation/>
                    </template>
                </Carousel>
            </div>        
        </div>
    </div>
</template>
