<template>
  <section class="py-20 gradient-section">
    <div class="flex w-full items-center justify-center gap-4 mb-12">
        <div class="h-px w-full bg-gradient-to-l from-slate-300 to-transparent" />
            <MessageCircle 
            :size="42"
            :stroke-width="1.5"
            class="flex-shrink-0 text-slate-500"
            />
        <div class="h-px w-full bg-gradient-to-r from-slate-300 to-transparent" />
    </div>
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="font-serif text-4xl md:text-5xl font-bold text-[#171940] mb-6">Como Funciona</h2>
        <p class="text-xl text-[#404259] max-w-3xl mx-auto leading-relaxed">
          Nosso processo é simples, transparente e focado em resultados. Veja como trabalhamos para resolver seu caso.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div
          v-for="(step, index) in steps"
          :key="index"
          class="card gradient-card border-none shadow-lg hover:shadow-xl transition-all duration-300 relative"
        >
          <div class="p-8 text-center">
            <div class="absolute -top-4 left-1/2 transform -translate-x-1/2">
              <div class="w-12 h-12 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full flex items-center justify-center">
                <span class="text-white font-bold text-lg">{{ step.number }}</span>
              </div>
            </div>

            <div class="mt-8 mb-6">
              <div class="w-16 h-16 bg-white rounded-full flex items-center justify-center mx-auto mb-4 shadow-md">
                <component :is="step.icon" class="w-8 h-8 text-[#171940]" />
              </div>
            </div>

            <h3 class="font-serif text-xl font-bold text-[#171940] mb-4">{{ step.title }}</h3>
            <p class="text-[#404259] leading-relaxed">{{ step.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { MessageSquare, Search, Target, MessageCircle } from 'lucide-vue-next'

const steps = [
  {
    icon: MessageSquare,
    number: "01",
    title: "Contato",
    description: "Entre em contato conosco através do WhatsApp, telefone ou formulário. Agende sua consulta inicial.",
  },
  {
    icon: Search,
    number: "02",
    title: "Análise",
    description: "Analisamos seu caso detalhadamente, identificando as melhores estratégias e caminhos legais.",
  },
  {
    icon: Target,
    number: "03",
    title: "Solução Personalizada",
    description: "Desenvolvemos uma estratégia personalizada e acompanhamos todo o processo até a resolução.",
  },
]
</script>
