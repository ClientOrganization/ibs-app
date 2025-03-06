<template>
  <button
    :class="[
      primaryClass
        ? 'bg-brand-primary hover:bg-brand-primary-hover text-white'
        : '',
      secondaryClass
        ? 'bg-brand-secondary hover:bg-brand-secondary-hover text-gray-800'
        : '',
      outlineClass
        ? 'bg-transparent border border-brand-primary text-brand-primary hover:bg-brand-primary hover:text-white'
        : '',
      'inline-flex items-center justify-center font-medium transition-colors duration-300 focus:outline-none focus:ring-2 focus:ring-offset-2 disabled:opacity-50 disabled:pointer-events-none rounded-md px-4 py-2',
    ]"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "BrandButton",
  props: {
    variant: {
      type: String,
      default: "primary",
      validator: function (value) {
        return ["primary", "secondary", "outline"].indexOf(value) !== -1;
      },
    },
    size: {
      type: String,
      default: "default",
      validator: function (value) {
        return ["sm", "default", "lg"].includes(value);
      },
    },
    type: {
      type: String,
      default: "button",
      validator: function (value) {
        return ["button", "submit", "reset"].includes(value);
      },
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    primaryClass() {
      return this.variant === "primary";
    },
    secondaryClass() {
      return this.variant === "secondary";
    },
    outlineClass() {
      return this.variant === "outline";
    },
  },
};
</script>

<style scoped>
/* Additional styling if needed */
</style>
