<template>
    <div v-for="row in numRows" :key="row" class="row" id="grid-rows">
        <div v-for="col in numCols" :key="col" class="col" id="grid-cols">
            <img v-if="(row-1)*numCols + col - 1 < direcciones.length" :src="direcciones[(row-1)*numCols + col - 1]" alt="">
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
    direcciones: {
        type: Array,
        default: () => []
    },
    numRows: {
        type: Number,
        default: 1
    },
    numCols: {
        type: Number,
        default: 4
    }
})
</script>