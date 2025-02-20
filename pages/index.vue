<template>
  <div class="bg-gray-900 text-white min-h-screen">
    <Header />
    <main class="pt-16">
      <HeroSection />
      <Features />
      <WhyBuildyUI />
      <LiveEditor /> 
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import HeroSection from '@/components/HeroSection.vue';
import Features from '@/components/Features.vue';
import WhyBuildyUI from '@/components/WhyBuildyUI.vue';
import LiveEditor from "@/components/LiveEditor.vue";
import Footer from '@/components/Footer.vue';

export default {
  name: 'IndexPage',
  components: {
    Header,
    HeroSection,
    Features,
    WhyBuildyUI,
    LiveEditor,
    Footer
  }
};
</script>

<style>
/* Ajout de styles optionnels si nécessaire */
</style>

