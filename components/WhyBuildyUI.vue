<template>
    <section class="bg-gray-800 text-white py-20 px-6">
      <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-12 items-center">
        <!-- Texte à gauche -->
        <div>
          <h2 class="text-4xl md:text-5xl font-extrabold mb-6 text-purple-400">Pourquoi choisir Buildy UI ?</h2>
          <p class="text-gray-300 text-lg">
            Un générateur de pages puissant, flexible et facile à utiliser, conçu pour vous aider à créer des interfaces modernes sans effort.
          </p>
        </div>
  
        <!-- Points clés à droite -->
        <div class="space-y-8">
          <div class="flex items-start space-x-4 transform transition hover:scale-105">
            <div class="w-20 h-20 flex items-center justify-center rounded-full">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7"></path>
              </svg>
            </div>
            <div>
              <h3 class="text-xl font-semibold">Simplicité et Rapidité</h3>
              <p class="text-gray-400">Glissez, déposez, personnalisez ! Créez des pages sans effort avec une interface intuitive.</p>
            </div>
          </div>
  
          <div class="flex items-start space-x-4 transform transition hover:scale-105">
            <div class="w-20 h-20 flex items-center justify-center rounded-full">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 8V16m-4-4h8"></path>
              </svg>
            </div>
            <div>
              <h3 class="text-xl font-semibold">100% Personnalisable</h3>
              <p class="text-gray-400">Adaptez chaque section à vos besoins avec une flexibilité totale sur le design.</p>
            </div>
          </div>
  
          <div class="flex items-start space-x-4 transform transition hover:scale-105">
            <div class="w-20 h-20 flex items-center justify-center rounded-full">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 10h11M9 21V3m6 18v-7m6 7v-4"></path>
              </svg>
            </div>
            <div>
              <h3 class="text-xl font-semibold">Optimisé et Léger</h3>
              <p class="text-gray-400">Performances optimisées pour une génération rapide et un code propre.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'WhyBuildyUI'
  };
  </script>
  
  <style>
  /* Ajout de styles optionnels si nécessaire */
  </style>
  