<template>
  <footer class="bg-[#171940] text-white py-16">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <!-- Logo and Description -->
        <div>
          <div class="flex items-center space-x-2 mb-6">
            <img :src="logoWhite" alt="logo ello advocacia" class="w-64" />
          </div>
          <p class="text-gray-300 leading-relaxed mb-6">
            Soluções jurídicas modernas com atendimento personalizado e compromisso com a excelência em cada caso.
          </p>
          <div class="flex space-x-4">
            <a
              href="https://linkedin.com/company/elloadvocacia"
              target="_blank"
              rel="noopener noreferrer"
              class="w-10 h-10 bg-white text-[#171940] border border-white rounded-full flex items-center justify-center hover:bg-[#171940] hover:text-[#FFFFFF] transition-colors"
            >
              <Linkedin class="w-5 h-5" />
            </a>
            <a
              href="https://wa.me/5511999999999"
              target="_blank"
              rel="noopener noreferrer"
              class="w-10 h-10 bg-white text-[#171940] border border-white rounded-full flex items-center justify-center hover:bg-[#171940] hover:text-[#FFFFFF]
              transition-colors"
            >
              <MessageCircle class="w-5 h-5" />
            </a>
            <a
              href="mailto:contato@elloadvocacia.com.br"
              class="w-10 h-10 bg-white text-[#171940] border border-white rounded-full flex items-center justify-center hover:bg-[#171940] hover:text-[#FFFFFF] transition-colors"
            >
              <Mail class="w-5 h-5" />
            </a>
          </div>
        </div>

        <!-- Contact Info -->
        <div>
          <h3 class="font-serif text-xl font-bold mb-6">Contato</h3>
          <div class="space-y-4 text-gray-300">
            <div>
              <p class="font-semibold text-white mb-1">Endereço</p>
              <p>Av. Paulista, 1000 - Sala 1501</p>
              <p>Bela Vista, São Paulo - SP</p>
              <p>CEP: 01310-100</p>
            </div>
            <div>
              <p class="font-semibold text-white mb-1">Telefones</p>
              <p>(11) 9999-9999</p>
              <p>(11) 3333-3333</p>
            </div>
            <div>
              <p class="font-semibold text-white mb-1">E-mail</p>
              <p>contato@elloadvocacia.com.br</p>
            </div>
          </div>
        </div>

        <!-- Legal Info -->
        <div>
          <h3 class="font-serif text-xl font-bold mb-6">Informações Legais</h3>
          <div class="space-y-4 text-gray-300">
            <div>
              <p class="font-semibold text-white mb-1">CNPJ</p>
              <p>12.345.678/0001-90</p>
            </div>
            <div>
              <p class="font-semibold text-white mb-1">Responsável Técnica</p>
              <p>Dra. Helena Moraes</p>
              <p>OAB/SP 123456</p>
            </div>
            <div>
              <p class="font-semibold text-white mb-1">Horário de Atendimento</p>
              <p>Segunda a Sexta: 8h às 18h</p>
              <p>Sábado: 8h às 12h</p>
            </div>
          </div>
        </div>
      </div>

      <div class="border-t border-[#404259] mt-12 pt-8 text-center">
        <p class="text-gray-300">© {{ currentYear }} Ello Advocacia. Todos os direitos reservados.</p>
        <p class="text-sm text-gray-400 mt-2">
          Este site é fictício e foi criado apenas para fins demonstrativos.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'
import { Linkedin, MessageCircle, Mail} from 'lucide-vue-next'
import logoWhite from '/images/logo/logo_white.png'

const currentYear = computed(() => new Date().getFullYear())
</script>
