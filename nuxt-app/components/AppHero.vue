<template>
  <section id="inicio" class="gradient-hero min-h-screen flex items-center relative overflow-hidden">
    <!-- Background geometric pattern -->
    <div class="absolute inset-0 opacity-10">
      <div class="absolute top-20 left-10 w-32 h-32 border border-white/20 rounded-full"></div>
      <div class="absolute top-40 right-20 w-24 h-24 border border-white/20 rotate-45"></div>
      <div class="absolute bottom-32 left-1/4 w-16 h-16 border border-white/20 rounded-full"></div>
      <div class="absolute bottom-20 right-1/3 w-20 h-20 border border-white/20 rotate-12"></div>
    </div>

    <div class="container mx-auto px-4 py-2 relative z-10">
      <div class="max-w-4xl mx-auto text-center text-white">
        <h1 class="font-serif text-4xl md:text-6xl lg:text-7xl font-bold mb-6 leading-tight">
          Soluções jurídicas modernas para <span class="text-[#928FA6]">desafios reais</span>
        </h1>

        <p class="text-lg md:text-2xl mb-8 text-gray-200 max-w-3xl mx-auto leading-relaxed">
          Oferecemos atendimento personalizado e estratégias inovadoras para proteger seus direitos e alcançar os
          melhores resultados em cada caso.
        </p>

        <div class="mb-12 flex justify-center">
        <button
            @click="scrollToContact"
            class="btn btn-primary flex items-center px-8 py-4 text-lg font-semibold rounded-full transition-all duration-300 transform hover:scale-105"
            style="background: linear-gradient(135deg, #928FA6 0%, white 100%); color: #171940;"
        >
            Agendar Consulta
            <ChevronRight class="w-5 h-5 ml-2" />
        </button>
        </div>


        <!-- Social Proof -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-2xl mx-auto">
          <div class="flex flex-col items-center">
            <div class="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center mb-3">
              <Clock class="w-6 h-6 text-[#928FA6]" />
            </div>
            <div class="text-2xl font-bold text-[#928FA6]">+10 anos</div>
            <div class="text-sm text-gray-300">de experiência</div>
          </div>

          <div class="flex flex-col items-center">
            <div class="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center mb-3">
              <Users class="w-6 h-6 text-[#928FA6]" />
            </div>
            <div class="text-2xl font-bold text-[#928FA6]">+300</div>
            <div class="text-sm text-gray-300">casos atendidos</div>
          </div>

          <div class="flex flex-col items-center">
            <div class="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center mb-3">
              <Award class="w-6 h-6 text-[#928FA6]" />
            </div>
            <div class="text-2xl font-bold text-[#928FA6]">98%</div>
            <div class="text-sm text-gray-300">de satisfação</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ChevronRight, Users, Award, Clock } from 'lucide-vue-next'

const scrollToContact = () => {
  const element = document.getElementById('contato')
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>
