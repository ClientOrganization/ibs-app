<template>
  <footer class="relative text-white py-16">
    <!-- Background image -->
    <div class="absolute inset-0 z-0">
      <img
        src="/footer-bg.jpg"
        alt="Shipping Background"
        class="w-full h-full object-cover opacity-30"
      />
    </div>

    <!-- Dark overlay -->
    <div class="absolute inset-0 bg-gray-900 opacity-80 z-0"></div>

    <!-- Content -->
    <div class="container mx-auto px-6 relative z-10">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <div>
          <div class="flex items-center space-x-4 mb-6">
            <img src="/logo.png" alt="IBS Logo" class="h-12" />
            <div>
              <h3 class="text-lg font-semibold">
                International Business Synergies
              </h3>
              <p class="text-xs text-gray-400">Trading FZCO</p>
            </div>
          </div>
          <p class="text-gray-400 max-w-xs">
            International Business Synergies Trading FZCO (IBS) is a global
            trading company specializing in energy, agriculture, and aquaculture
            commodities.
          </p>
        </div>
        <div>
          <h3 class="text-xl font-semibold mb-6">Contact Us</h3>
          <address class="not-italic text-gray-400">
            <p>International Business Synergies Trading FZCO</p>
            <p>Dubai Silicon Oasis</p>
            <p>DBP Building, A1</p>
            <p>Dubai, United Arab Emirates</p>
            <p class="mt-4">Phone: +971 58-627-1722</p>
            <p class="mt-1">Email: info@ibsltd.com</p>
          </address>
        </div>
        <div>
          <h3 class="text-xl font-semibold mb-4">Stay up to date</h3>
          <form class="flex flex-col sm:flex-row">
            <input
              type="email"
              placeholder="Email"
              required
              class="px-4 py-2 bg-gray-800 text-white focus:outline-none rounded-l"
            />
            <button
              type="submit"
              class="bg-blue-600 hover:bg-blue-700 px-6 py-2 rounded-r font-medium transition-colors duration-300"
            >
              Sign Up
            </button>
          </form>
        </div>
      </div>
      <div
        class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-500"
      >
        <p>© 2025 International Business Synergies. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
// Footer functionality can be added here
</script>

<style scoped>
/* Add your styles here */
footer::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #1e40af, #3b82f6, #60a5fa);
}

/* Additional background image styling */
footer {
  background-position: center;
  background-size: cover;
}
</style>
