<template>
  <header
    class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-md border-b"
  >
    <div class="container mx-auto px-6 py-4 flex justify-between items-center">
      <div class="flex items-center space-x-4">
        <img src="/logo.png" alt="IBS Logo" class="h-10" />
        <div class="hidden md:block">
          <h1 class="text-lg font-semibold text-gray-900">
            International Business Synergies
          </h1>
          <p class="text-xs text-gray-500">Trading FZCO</p>
        </div>
      </div>
      <nav class="hidden md:block">
        <ul class="flex space-x-8">
          <li>
            <a
              href="#about"
              class="text-gray-800 hover:text-blue-600 transition-colors duration-300 font-medium"
              >About Us</a
            >
          </li>
          <li>
            <a
              href="#global-trade"
              class="text-gray-800 hover:text-blue-600 transition-colors duration-300 font-medium"
              >Global Trade</a
            >
          </li>
          <li>
            <a
              href="#energy"
              class="text-gray-800 hover:text-blue-600 transition-colors duration-300 font-medium"
              >Energy</a
            >
          </li>
          <li>
            <a
              href="#commodities"
              class="text-gray-800 hover:text-blue-600 transition-colors duration-300 font-medium"
              >Commodities</a
            >
          </li>
          <li>
            <a
              href="#contact"
              class="text-gray-800 hover:text-blue-600 transition-colors duration-300 font-medium"
              >Contact</a
            >
          </li>
        </ul>
      </nav>
      <button class="block md:hidden focus:outline-none">
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          ></path>
        </svg>
      </button>
    </div>
  </header>
</template>

<script setup lang="ts">
// Mobile menu functionality can be added here
</script>

<style scoped>
header {
  backdrop-filter: blur(5px);
  background-color: rgba(255, 255, 255, 0.9);
}
</style>
