<template>
  <footer class="bg-gray-900 text-white py-10 mt-16">
    <div class="container mx-auto px-6 md:px-12">
      <div class="grid md:grid-cols-4 gap-8">
        
        <!-- Logo & Slogan -->
        <div>
          <div class="flex flex-row items-center">
            <img src="/images/logo.png" alt="Buildy UI" class="h-12 mb-4">
            <span class="text-xl font-bold">Buildy UI</span>
          </div>
          <p class="text-gray-400 text-sm">Un outil puissant et flexible pour créer des interfaces modernes avec Tailwind CSS.</p>
        </div>

        <!-- Liens utiles -->
        <div>
          <h3 class="text-lg font-semibold mb-4 text-purple-400">Liens rapides</h3>
          <ul class="space-y-2">
            <li><a href="#" class="text-gray-300 hover:text-purple-400 transition">Accueil</a></li>
            <li><a href="#" class="text-gray-300 hover:text-purple-400 transition">Fonctionnalités</a></li>
            <li><a href="#" class="text-gray-300 hover:text-purple-400 transition">Documentation</a></li>
            <li><a href="#" class="text-gray-300 hover:text-purple-400 transition">Contact</a></li>
          </ul>
        </div>

        <!-- Réseaux sociaux -->
        <div>
          <h3 class="text-lg font-semibold mb-4 text-purple-400">Suivez-nous</h3>
          <div class="flex space-x-6 mx-auto">
            <a href="#" class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 2.04c-5.52 0-10 4.48-10 10 0 4.42 2.87 8.17 6.84 9.5.5.09.68-.22.68-.5v-1.76c-2.78.61-3.37-1.34-3.37-1.34-.46-1.17-1.12-1.48-1.12-1.48-.91-.63.07-.62.07-.62 1 .07 1.53 1.04 1.53 1.04.89 1.53 2.33 1.09 2.9.83.09-.65.35-1.09.63-1.34-2.22-.25-4.56-1.11-4.56-4.95 0-1.09.39-1.98 1.04-2.68-.1-.26-.45-1.27.1-2.65 0 0 .84-.27 2.75 1.02A9.43 9.43 0 0112 6.8c.85 0 1.7.11 2.5.32 1.9-1.29 2.74-1.02 2.74-1.02.55 1.38.2 2.39.1 2.65.65.7 1.04 1.59 1.04 2.68 0 3.86-2.34 4.7-4.58 4.95.36.31.68.93.68 1.88v2.78c0 .28.18.6.69.5A10.02 10.02 0 0022 12.04c0-5.52-4.48-10-10-10z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path d="M22.23 5.924c-.793.35-1.644.586-2.54.693a4.48 4.48 0 001.972-2.475 8.947 8.947 0 01-2.838 1.083 4.463 4.463 0 00-7.655 4.067 12.69 12.69 0 01-9.217-4.67 4.469 4.469 0 001.384 5.956 4.418 4.418 0 01-2.022-.56v.057c0 2.08 1.476 3.82 3.436 4.216a4.5 4.5 0 01-2.014.076 4.471 4.471 0 004.17 3.1 8.963 8.963 0 01-5.553 1.913c-.362 0-.72-.021-1.075-.062a12.676 12.676 0 006.89 2.013c8.27 0 12.8-6.856 12.8-12.801 0-.195-.005-.389-.013-.583a9.176 9.176 0 002.25-2.34z"/>
              </svg>
            </a>
          </div>
        </div>

        <!-- Newsletter -->
        <div>
          <h3 class="text-lg font-semibold mb-4 text-purple-400">Abonnez-vous à la newsletter</h3>
          <form @submit.prevent="subscribe">
            <div class="flex items-center">
              <input 
                type="email" 
                v-model="email"
                placeholder="Votre email" 
                class="w-full p-3 rounded-l-lg bg-gray-800 text-white placeholder-gray-400 border border-gray-700 focus:border-purple-500 focus:ring focus:ring-purple-400 outline-none"
                required
              />
              <button 
                type="submit" 
                class="bg-purple-400 hover:bg-purple-500 text-white px-4 py-3 rounded-r-lg transition">
                S'inscrire
              </button>
            </div>
          </form>
        </div>

      </div>

      <!-- Copyright -->
      <div class="text-center text-gray-500 text-sm mt-8 border-t border-gray-700 pt-4">
        &copy; 2025 Buildy UI. Tous droits réservés.
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      email: '',
    };
  },
  methods: {
    subscribe() {
      alert(`Merci pour votre inscription, ${this.email} !`);
      this.email = '';
    },
  },
};
</script>
