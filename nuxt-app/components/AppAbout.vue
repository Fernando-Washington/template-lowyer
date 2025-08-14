<template>
  <section id="sobre" class="py-20 bg-white">
    <div class="flex w-full items-center justify-center gap-4 mb-12">
        <div class="h-px w-full bg-gradient-to-l from-slate-300 to-transparent" />
            <GraduationCap
            :size="48"
            :stroke-width="1.5"
            class="flex-shrink-0 text-slate-500"
            />
        <div class="h-px w-full bg-gradient-to-r from-slate-300 to-transparent" />
    </div>
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <div>
          <h2 class="font-serif text-4xl md:text-5xl font-bold text-[#171940] mb-6">Quem Somos</h2>
          <p class="text-lg text-[#404259] mb-6 leading-relaxed">
            A Ello Advocacia nasceu da visão de transformar a advocacia tradicional, oferecendo soluções jurídicas
            modernas e acessíveis. Nossa missão é proporcionar segurança jurídica com atendimento próximo e
            personalizado.
          </p>
          <p class="text-lg text-[#404259] mb-8 leading-relaxed">
            Liderada pela <strong>Dra. Helena Moraes – OAB/SP 123456</strong>, nossa equipe combina experiência sólida
            com inovação, garantindo que cada cliente receba a atenção e expertise que merece.
          </p>

          <div class="space-y-4">
            <div v-for="(value, index) in values" :key="index" class="flex items-center space-x-3">
              <CheckCircle class="w-6 h-6 text-[#928FA6] flex-shrink-0" />
              <span class="text-[#404259] font-medium">{{ value }}</span>
            </div>
          </div>
        </div>

        <div class="relative">
          <div class="card gradient-card border-none shadow-xl">
            <div class="p-8">
              <div class="text-center">
                <div class="w-24 h-24 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full mx-auto mb-6 flex items-center justify-center">
                  <span class="text-white font-serif text-2xl font-bold">HM</span>
                </div>
                <h3 class="font-serif text-2xl font-bold text-[#171940] mb-2">Dra. Helena Moraes</h3>
                <p class="text-[#928FA6] font-medium mb-4">OAB/SP 123456</p>
                <p class="text-[#404259] leading-relaxed">
                  Especialista em Direito Civil e de Família, com pós-graduação em Direito Digital. Mais de 10 anos de
                  experiência defendendo os direitos de nossos clientes com dedicação e excelência.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { CheckCircle, GraduationCap } from 'lucide-vue-next'

const values = [
  "Atendimento personalizado e humanizado",
  "Transparência em todos os processos",
  "Estratégias inovadoras e eficazes",
  "Compromisso com a ética profissional",
]
</script>
