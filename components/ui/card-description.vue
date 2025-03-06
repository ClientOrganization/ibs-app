<script setup lang="ts">
defineProps<{
  className?: string;
}>();
</script>

<template>
  <p class="text-sm text-muted-foreground" :class="className">
    <slot></slot>
  </p>
</template>

<style scoped>
:global(.text-muted-foreground) {
  color: #6b7280;
}
</style>
