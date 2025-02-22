<template>
    <div class="bg-gray-900 text-white min-h-screen p-4">
        <Header />
        <main>
          <ContactForm />
        </main>
        <Footer />

    </div>
</template>

<script>
import Header from '@/components/Header.vue';
import ContactForm from '@/components/ContactForm.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'FeaturesPage',
  components: {
    Header,
    ContactForm,
    Footer

  }
};
</script>