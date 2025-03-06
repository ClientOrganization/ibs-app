<script setup lang="ts">
defineProps<{
  className?: string;
}>();
</script>

<template>
  <div class="flex items-center p-6 pt-0" :class="className">
    <slot></slot>
  </div>
</template>
