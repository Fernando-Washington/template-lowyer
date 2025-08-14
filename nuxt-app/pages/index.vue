<template>
  <main class="min-h-screen font-sans text-[#404259]">
    <AppHeader />
    <AppHero />
    <AppServices />
    <AppAbout />
    <AppProcess />
    <AppTestimonials />
    <AppContact />
    <AppFooter />
  </main>
</template>

<script setup>
import AppHeader from '@/components/AppHeader.vue'
import AppHero from '@/components/AppHero.vue'
import AppServices from '@/components/AppServices.vue'
import AppAbout from '@/components/AppAbout.vue'
import AppProcess from '@/components/AppProcess.vue'
import AppTestimonials from '@/components/AppTestimonials.vue'
import AppContact from '@/components/AppContact.vue'
import AppFooter from '@/components/AppFooter.vue'
</script>

<style>
html {
  scroll-behavior: smooth;
}
/* Removed Tailwind configurations, keeping only custom fonts and gradients */
/* Fontes externas */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=DM+Sans:wght@300;400;500;600&display=swap');

/* Fontes customizadas aplicáveis via Tailwind */
.font-sans {
  font-family: 'DM Sans', sans-serif;
}

/* Font serif para títulos */
.font-serif {
  font-family: 'Playfair Display', serif;
}

/* Gradientes personalizados */
.gradient-hero {
  background: linear-gradient(135deg, #171940 0%, #1E2040 50%, #928FA6 100%);
}

.gradient-section {
  background: linear-gradient(135deg, #F2F2F2 0%, rgba(146, 143, 166, 0.1) 100%);
}

.gradient-card {
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.9) 0%, rgba(146, 143, 166, 0.05) 100%);
  backdrop-filter: blur(10px);
}
</style>
