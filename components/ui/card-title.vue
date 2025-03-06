<script setup lang="ts">
defineProps<{
  className?: string;
}>();
</script>

<template>
  <h3
    class="text-2xl font-semibold leading-none tracking-tight"
    :class="className"
  >
    <slot></slot>
  </h3>
</template>
