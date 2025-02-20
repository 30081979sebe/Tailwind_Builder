<template>
  <section class="relative bg-gray-900 text-white min-h-screen flex flex-col justify-center items-center text-center px-6 py-24">
    <!-- Effet d'onde de fond -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-0 left-0 w-full h-full opacity-20 bg-gradient-to-b from-purple-700 to-gray-900"></div>
      <svg class="absolute top-0 left-0 w-full opacity-10" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path fill="rgb(100,72,153)" fill-opacity="1" 
              d="M0,160L80,133.3C160,107,320,53,480,85.3C640,117,800,235,960,245.3C1120,256,1280,160,1360,106.7L1440,53L1440,0L1360,0C1280,0,1120,0,960,0C800,0,640,0,480,0C320,0,160,0,80,0L0,0Z">
        </path>
      </svg>
    </div>

    <div class="relative z-10 max-w-3xl">
      <h2 class="text-5xl md:text-7xl font-extrabold mb-6">
        <span class="text-purple-400 mb-4">Buildy Ui</span>
        <p>L'outil ultime de création</p>
      </h2>
      <p class="text-lg md:text-xl text-gray-300 mb-6">
        Construisez des pages modernes et élégantes avec un générateur visuel basé sur Tailwind CSS.
      </p>
      <div class="flex justify-center gap-4">
        <button class="bg-purple-600 hover:bg-purple-500 text-white font-bold py-4 px-8 rounded-lg shadow-lg transition transform hover:scale-105">
          Commencer maintenant
        </button>
        <button class="hover:bg-gray-600 text-white font-bold py-4 px-8 rounded-lg shadow-lg transition transform hover:scale-105">
          En savoir plus
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HeroSection",
};
</script>

<style>
/* Ajout de styles optionnels si nécessaire */
</style>
