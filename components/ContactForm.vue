<template>
    <div class="container mx-auto mt-20">
        <h1 class="text-4xl font-bold text-violet-500 mb-8 text-center">Contactez-nous</h1>
        
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        <!-- Carte et informations -->
        <div class="space-y-6">
            <div id="map" class="w-full h-[400px] rounded-lg shadow-xl"></div>
            
            <div class="bg-black rounded-lg shadow-xl p-6 space-y-4">
            <div class="flex items-center space-x-3 text-violet-400">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
                <span>123 Rue Example, 75000 Paris</span>
            </div>
            
            <div class="flex items-center space-x-3 text-violet-400">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                </svg>
                <span><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2b4844455f4a485f6b4e534a465b474e05484446">[email&#160;protected]</a></span>
            </div>
            
            <div class="flex items-center space-x-3 text-violet-400">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                </svg>
                <span>+33 1 23 45 67 89</span>
            </div>
            </div>
        </div>

        <!-- Formulaire -->
        <div class="bg-black rounded-lg shadow-xl p-8">
            <form id="contactForm" class="space-y-6">
            <div>
                <label for="name" class="block text-violet-400 mb-2">Nom</label>
                <input type="text" id="name" name="name" required
                class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-violet-500 focus:outline-none focus:ring-2 focus:ring-violet-600">
            </div>

            <div>
                <label for="email" class="block text-violet-400 mb-2">Email</label>
                <input type="email" id="email" name="email" required
                class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-violet-500 focus:outline-none focus:ring-2 focus:ring-violet-600">
            </div>

            <div>
                <label for="subject" class="block text-violet-400 mb-2">Sujet</label>
                <input type="text" id="subject" name="subject" required
                class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-violet-500 focus:outline-none focus:ring-2 focus:ring-violet-600">
            </div>

            <div>
                <label for="message" class="block text-violet-400 mb-2">Message</label>
                <textarea id="message" name="message" rows="4" required
                class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-violet-500 focus:outline-none focus:ring-2 focus:ring-violet-600 resize-none"></textarea>
            </div>

            <button type="submit" 
                class="w-full py-3 px-4 bg-violet-600 text-white rounded-md hover:bg-violet-700 transition duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-violet-500">
                Envoyer
            </button>
            </form>
        </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'ContactForm'
};

</script>

<style>
/* Animations pour les inputs */
input, textarea {
  transition: all 0.3s ease;
}

input:focus, textarea:focus {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(139, 92, 246, 0.25);
}

/* Animation pour le formulaire */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

form, #map {
  animation: fadeIn 0.6s ease-out;
}

/* Style pour la carte */
#map {
  border: 2px solid #8B5CF6;
  transition: all 0.3s ease;
}

#map:hover {
  box-shadow: 0 0 20px rgba(139, 92, 246, 0.3);
}
</style>