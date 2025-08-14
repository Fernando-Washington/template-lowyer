<template>
  <section id="areas" class="py-20 gradient-section">
    <div class="flex w-full items-center justify-center gap-4 mb-12">
        <div class="h-px w-full bg-gradient-to-l from-slate-300 to-transparent" />
            <BriefcaseBusiness 
            :size="42"
            :stroke-width="1.5"
            class="flex-shrink-0 text-slate-500"
            />
        <div class="h-px w-full bg-gradient-to-r from-slate-300 to-transparent" />
    </div>
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="font-serif text-4xl md:text-5xl font-bold text-[#171940] mb-6">Áreas de Atuação</h2>
        <p class="text-xl text-[#404259] max-w-3xl mx-auto leading-relaxed">
          Oferecemos serviços especializados em diversas áreas do direito, sempre com foco na excelência e no
          atendimento personalizado.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div
          v-for="(service, index) in services"
          :key="index"
          class="card gradient-card border-none shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
        >
          <div class="p-8 text-center">
            <div class="w-16 h-16 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full flex items-center justify-center mx-auto mb-6">
              <component :is="service.icon" class="w-8 h-8 text-white" />
            </div>
            <h3 class="font-serif text-xl font-bold text-[#171940] mb-4">{{ service.title }}</h3>
            <p class="text-[#404259] leading-relaxed">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Heart, Briefcase, Scale, Smartphone, BriefcaseBusiness} from 'lucide-vue-next'

const services = [
  {
    icon: Heart,
    title: "Direito de Família",
    description: "Divórcio, guarda, pensão alimentícia e questões familiares com sensibilidade e expertise.",
  },
  {
    icon: Briefcase,
    title: "Direito Trabalhista",
    description: "Defesa dos direitos trabalhistas, rescisões, horas extras e questões previdenciárias.",
  },
  {
    icon: Scale,
    title: "Direito Civil",
    description: "Contratos, indenizações, cobranças e resolução de conflitos entre particulares.",
  },
  {
    icon: Smartphone,
    title: "Direito Digital",
    description: "LGPD, crimes virtuais, proteção de dados e questões relacionadas ao mundo digital.",
  },
]
</script>
