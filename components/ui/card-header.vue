<script setup lang="ts">
defineProps<{
  className?: string;
}>();
</script>

<template>
  <div class="flex flex-col space-y-1.5 p-6" :class="className">
    <slot></slot>
  </div>
</template>
