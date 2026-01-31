<script setup lang="ts">
// app shell: keep layout as a column so footer can be pushed to the bottom.
</script>

<template>
  <div class="app-root">
    <Header/>
    <main class="content">
      <NuxtPage />
    </main>
    <Footer/>
  </div>
</template>
