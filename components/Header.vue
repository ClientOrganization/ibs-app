<template>
  <header
    class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-md border-b border-brand-secondary"
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
            <a href="#about" class="nav-link">About Us</a>
          </li>
          <li>
            <a href="#global-trade" class="nav-link">Global Trade</a>
          </li>
          <li>
            <a href="#energy" class="nav-link">Energy</a>
          </li>
          <li>
            <a href="#commodities" class="nav-link">Commodities</a>
          </li>
          <li>
            <a href="#contact" class="nav-link contact-button">Contact</a>
          </li>
        </ul>
      </nav>
      <button class="block md:hidden focus:outline-none text-brand-primary">
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

.nav-link {
  color: #333;
  font-weight: 500;
  transition: color 0.3s ease;
  position: relative;
}

.nav-link:hover {
  color: var(--primary-color);
}

.nav-link::after {
  content: "";
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: var(--primary-color);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.contact-button {
  color: var(--primary-color);
  font-weight: 600;
}

.contact-button:hover {
  color: var(--primary-hover);
}

.border-brand-secondary {
  border-color: var(--secondary-color);
  border-bottom-width: 3px;
}

.text-brand-primary {
  color: var(--primary-color);
}
</style>
