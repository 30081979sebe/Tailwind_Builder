<template>
  <section class="bg-gray-900 text-white py-24 px-6">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-4xl md:text-5xl font-extrabold mb-8 text-purple-400">Comment fonctionne Buildy UI ?</h2>
      <p class="text-gray-300 mb-12 max-w-3xl mx-auto">
        Un processus simple et efficace pour créer des pages modernes en quelques clics.
      </p>
    </div>

    <!-- Timeline -->
    <div class="relative max-w-6xl mx-auto">
      <div class="border-l-4 border-purple-500 absolute left-1/2 transform -translate-x-1/2 h-full hidden md:block"></div>

      <div class="grid md:grid-cols-2 gap-8 relative">
        <!-- Étape 1 -->
        <div class="flex flex-col items-center text-center md:text-left md:items-start space-y-4">
          <div class="w-10 h-10 flex items-center justify-center bg-purple-500 rounded-full text-white font-bold transition transform hover:scale-110 hover:bg-purple-400">1</div>
          <h3 class="text-xl font-semibold">Sélectionnez un template</h3>
          <p class="text-gray-400">Choisissez un modèle préconçu ou démarrez avec une page vierge.</p>
        </div>

        <!-- Étape 2 -->
        <div class="flex flex-col items-center text-center md:text-right md:items-end space-y-4">
          <div class="w-10 h-10 flex items-center justify-center bg-purple-500 rounded-full text-white font-bold transition transform hover:scale-110 hover:bg-purple-400">2</div>
          <h3 class="text-xl font-semibold">Personnalisez avec l’éditeur</h3>
          <p class="text-gray-400">Ajoutez, modifiez et organisez les composants visuels à votre guise.</p>
        </div>

        <!-- Étape 3 -->
        <div class="flex flex-col items-center text-center md:text-left md:items-start space-y-4">
          <div class="w-10 h-10 flex items-center justify-center bg-purple-500 rounded-full text-white font-bold transition transform hover:scale-110 hover:bg-purple-400">3</div>
          <h3 class="text-xl font-semibold">Prévisualisez en temps réel</h3>
          <p class="text-gray-400">Voyez immédiatement les modifications et ajustez-les en conséquence.</p>
        </div>

        <!-- Étape 4 -->
        <div class="flex flex-col items-center text-center md:text-right md:items-end space-y-4">
          <div class="w-10 h-10 flex items-center justify-center bg-purple-500 rounded-full text-white font-bold transition transform hover:scale-110 hover:bg-purple-400">4</div>
          <h3 class="text-xl font-semibold">Exportation optimisée</h3>
          <p class="text-gray-400">Téléchargez votre page avec un code propre et optimisé.</p>
        </div>
      </div>
    </div>

  </section>
</template>

<script>
export default {
  name: 'Features'
};
</script>

<style>
/* Ajout de styles optionnels si nécessaire */
</style>
