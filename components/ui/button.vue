<script setup lang="ts">
const props = defineProps({
  size: {
    type: String,
    default: "default",
    validator: (value: string) => ["default", "sm", "lg"].includes(value),
  },
  variant: {
    type: String,
    default: "default",
    validator: (value: string) =>
      [
        "default",
        "destructive",
        "outline",
        "secondary",
        "ghost",
        "link",
      ].includes(value),
  },
  asChild: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <button
    class="inline-flex items-center justify-center rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:opacity-50 disabled:pointer-events-none"
    :class="[
      variant === 'default' && 'bg-blue-600 text-white hover:bg-blue-700',
      variant === 'destructive' && 'bg-red-600 text-white hover:bg-red-700',
      variant === 'outline' &&
        'border border-gray-300 hover:bg-gray-100 hover:text-gray-900',
      variant === 'secondary' && 'bg-gray-200 text-gray-900 hover:bg-gray-300',
      variant === 'ghost' && 'hover:bg-gray-100 hover:text-gray-900',
      variant === 'link' && 'underline-offset-4 hover:underline text-blue-600',
      size === 'default' && 'h-10 py-2 px-4',
      size === 'sm' && 'h-9 px-3 rounded-md',
      size === 'lg' && 'h-11 px-8 rounded-md',
    ]"
  >
    <slot></slot>
  </button>
</template>

<script>
// Add a default export to fix import issues
export default {
  name: "Button",
};
</script>
