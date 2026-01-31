<template>
    <button
    type="button"
    class="btn btn-info btn-lg btn-hvr"
    @click="openModal"
    >
    Conoce más 👉
    </button>

    <div class="modal fade" ref="modalRef" @keydown.esc="closeModal">
    <div class="modal-dialog">
        <div class="modal-content">

        <div class="modal-header">
            <h5 class="modal-title">{{ titulo }}</h5>
            <button type="button" class="btn-close" @click="closeModal"></button>
        </div>

        <div class="modal-body">
            <p>{{ texto }}</p>
        </div>

        <div class="modal-footer">
            <button type="button" class="btn btn-secondary" @click="closeModal">
            Cerrar
            </button>
        </div>

        </div>
    </div>
    </div>

    <div v-if="isOpen" class="modal-backdrop fade show" @click="closeModal"></div>

</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
    titulo: String,
    texto: String
})

const modalRef = ref()
const isOpen = ref(false)

const openModal = () => {
  const modalElement = modalRef.value
  if (modalElement) {
    modalElement.classList.add('show')
    modalElement.style.display = 'block'
    document.body.classList.add('modal-open')
    isOpen.value = true
  }
}

const closeModal = () => {
  const modalElement = modalRef.value
  if (modalElement) {
    modalElement.classList.remove('show')
    modalElement.style.display = 'none'
    document.body.classList.remove('modal-open')
    isOpen.value = false
  }
}
</script>