<template>
  <header
    :class="[
      'sticky top-0 left-0 right-0 z-50 transition-all duration-300',
      isScrolled ? 'bg-white/95 backdrop-blur-md shadow-lg' : 'bg-[#FFFFFF]'
    ]"
  >
    <div class="container mx-auto px-4 py-4">
      <div class="flex items-center justify-between">
        <!-- Logo -->
        <div class="flex items-center space-x-2">
          <a href="#top">
            <img :src="imgLogo" alt="logo ello advocacaia" class="w-full h-10" />
          </a>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center space-x-8">
          <button
            @click="scrollToSection('inicio')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium"
          >
            Início
          </button>
          <button
            @click="scrollToSection('areas')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium"
          >
            Áreas de Atuação
          </button>
          <button
            @click="scrollToSection('sobre')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium"
          >
            Sobre
          </button>
          <button
            @click="scrollToSection('contato')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium"
          >
            Contato
          </button>
        </nav>

        <!-- CTA Button -->
        <div class="hidden md:block">
          <button
            @click="handleWhatsAppClick"
            class="btn btn-primary px-6 py-2 rounded-full flex items-center"
          >
            <MessageCircle class="w-4 h-4 mr-2" />
            Fale Conosco
          </button>
        </div>

        <!-- Mobile Menu Button -->
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden p-2 text-[#171940]">
          <X v-if="isMenuOpen" class="w-6 h-6" />
          <Menu v-else class="w-6 h-6" />
        </button>
      </div>

      <!-- Mobile Menu -->
      <div v-if="isMenuOpen" class="md:hidden mt-4 py-4 bg-white rounded-lg shadow-lg">
        <nav class="flex flex-col space-y-4 px-4">
          <button
            @click="scrollToSection('inicio')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium text-left"
          >
            Início
          </button>
          <button
            @click="scrollToSection('areas')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium text-left"
          >
            Áreas de Atuação
          </button>
          <button
            @click="scrollToSection('sobre')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium text-left"
          >
            Sobre
          </button>
          <button
            @click="scrollToSection('contato')"
            class="text-[#404259] hover:text-[#171940] transition-colors font-medium text-left"
          >
            Contato
          </button>
          <button
            @click="handleWhatsAppClick"
            class="btn btn-primary w-full mt-4 border border-[#171940] rounded-full flex items-center justify-center py-2"
          >
            Fale Conosco
          </button>
        </nav>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { Menu, X, MessageCircle } from 'lucide-vue-next'
import imgLogo from '/images/logo/logo.png'

const isMenuOpen = ref(false)
const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
    isMenuOpen.value = false
  }
}

const handleWhatsAppClick = () => {
  window.open('https://wa.me/5511999999999?text=Olá! Gostaria de agendar uma consulta.', '_blank')
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>