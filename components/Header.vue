<template>
  <header class="bg-gray-900 text-white p-4 fixed w-full top-0 z-50 shadow-md opacity-90">
    <div class="container mx-auto flex justify-between items-center">
      <!-- Logo (Agrandissement en mobile) -->
      <a href="/" class="flex items-center space-x-2 md:pl-4 mx-auto md:mx-0">
        <img src="/images/logo.png" alt="Buildy UI" class="h-14 w-14 md:h-10 md:w-10">
        <span class="text-xl font-bold">Buildy UI</span>
      </a>

      <!-- Desktop Menu -->
      <nav class="hidden md:flex space-x-6">
        <NuxtLink to="/" class="hover:text-purple-400">Accueil</NuxtLink>
        <NuxtLink to="/features" class="hover:text-purple-400">Fonctionnalités</NuxtLink>
        <NuxtLink to="/contact" class="hover:text-purple-400">Contact</NuxtLink>
      </nav>

      <!-- Mobile Menu Button -->
      <button @click="toggleMenu" class="md:hidden focus:outline-none">
        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <transition name="fade">
      <nav v-if="isMenuOpen" class="md:hidden fixed top-0 left-0 w-full h-full bg-gray-900 bg-opacity-90 flex flex-col justify-center items-center space-y-6">
        <a href="#" class="text-lg text-white hover:text-purple-400 transition">Accueil</a>
        <a href="#" class="text-lg text-white hover:text-purple-400 transition">Fonctionnalités</a>
        <a href="#" class="text-lg text-white hover:text-purple-400 transition">Contact</a>
        <button @click="toggleMenu" class="mt-6 text-gray-400 hover:text-white transition">Fermer</button>
      </nav>
    </transition>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style>
/* Animation du menu mobile */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s ease-in-out;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
