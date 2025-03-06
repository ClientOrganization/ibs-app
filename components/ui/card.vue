<script setup lang="ts">
const props = defineProps({
  className: {
    type: String,
    default: "",
  },
});
</script>

<template>
  <div
    class="rounded-lg border bg-card text-card-foreground shadow-sm"
    :class="className"
  >
    <slot></slot>
  </div>
</template>

<style scoped>
:global(.bg-card) {
  background-color: white;
}
:global(.text-card-foreground) {
  color: #1f2937;
}
</style>
