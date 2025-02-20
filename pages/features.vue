<template>
    <div class="bg-gray-900 text-white min-h-screen">
        <Header />
        <main>
          <HeroFonctionnality />
          <Fonctionnality />

        </main>
        <Footer />

    </div>
</template>

<script>
import Header from '@/components/Header.vue';
import HeroFonctionnality from '@/components/HeroFonctionnality.vue';
import Fonctionnality from '@/components/Fonctionnality.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'FeaturesPage',
  components: {
    Header,
    HeroFonctionnality,
    Fonctionnality,
    Footer
  }
};
</script>

<style scoped>
/* Ajout possible d'animations ou d'effets */
</style>