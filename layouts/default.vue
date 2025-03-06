<script setup lang="ts">
// Components are auto-imported with script setup
</script>

<template>
  <div class="min-h-screen flex flex-col bg-white">
    <Header />
    <main class="flex-grow">
      <slot />
    </main>
    <Footer />
  </div>
</template>

<style scoped>
/* Smooth scrolling */
:global(html) {
  scroll-behavior: smooth;
}
</style>
