<template>
  <section class="py-20 bg-white">
    <div class="flex w-full items-center justify-center gap-4 mb-12">
        <div class="h-px w-full bg-gradient-to-l from-slate-300 to-transparent" />
            <Quote  
            :size="42"
            :stroke-width="1.5"
            class="flex-shrink-0 text-slate-500"
            />
        <div class="h-px w-full bg-gradient-to-r from-slate-300 to-transparent" />
    </div>
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="font-serif text-4xl md:text-5xl font-bold text-[#171940] mb-6">O que nossos clientes dizem</h2>
        <p class="text-xl text-[#404259] max-w-3xl mx-auto leading-relaxed">
          A satisfação dos nossos clientes é nossa maior conquista. Veja alguns depoimentos de quem confiou em nosso
          trabalho.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 rounded-lg p-8">
        <div
          v-for="(testimonial, index) in testimonials"
          :key="index"
          class="card gradient-card shadow-lg hover:shadow-xl transition-all duration-300 border rounded-sm border-[#928FA61A]"
        >
          <div class="p-8">
            <div class="mb-6">
              <Quote class="w-8 h-8 text-[#928FA6] mb-4" />
              <p class="text-[#404259] leading-relaxed italic">"{{ testimonial.content }}"</p>
            </div>

            <div class="flex items-center mb-4">
              <Star
                v-for="i in testimonial.rating"
                :key="i"
                class="w-5 h-5 text-yellow-400 fill-current"
              />
            </div>

            <div>
              <h4 class="font-semibold text-[#171940] mb-1">{{ testimonial.name }}</h4>
              <p class="text-[#928FA6] text-sm">{{ testimonial.role }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Star, Quote } from 'lucide-vue-next'

const testimonials = [
  {
    name: "Maria Silva",
    role: "Empresária",
    content:
      "A Ello Advocacia me ajudou em um processo trabalhista complexo. O atendimento foi excepcional e o resultado superou minhas expectativas. Recomendo sem hesitar!",
    rating: 5,
  },
  {
    name: "João Santos",
    role: "Contador",
    content:
      "Precisava de ajuda com questões contratuais e a equipe da Dra. Helena foi muito profissional. Resolveram tudo de forma rápida e eficiente.",
    rating: 5,
  },
  {
    name: "Ana Costa",
    role: "Arquiteta",
    content:
      "Excelente escritório! Me auxiliaram em um processo de divórcio com muito cuidado e sensibilidade. Senti-me acolhida durante todo o processo.",
    rating: 5,
  },
]
</script>
