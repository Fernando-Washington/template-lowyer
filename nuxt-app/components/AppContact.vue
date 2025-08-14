<template>
    <section id="contato" class="py-20 gradient-section">
    <div class="flex w-full items-center justify-center gap-4 mb-12">
        <div class="h-px w-full bg-gradient-to-l from-slate-300 to-transparent" />
            <Mail 
            :size="42"
            :stroke-width="1.5"
            class="flex-shrink-0 text-slate-500"
            />
        <div class="h-px w-full bg-gradient-to-r from-slate-300 to-transparent" />
    </div>
        <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="font-serif text-4xl md:text-5xl font-bold text-[#171940] mb-6">Entre em Contato</h2>
        <p class="text-xl text-[#404259] max-w-3xl mx-auto leading-relaxed">
          Estamos prontos para ajudar você. Entre em contato conosco e agende sua consulta para discutir seu caso.
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
        <!-- Contact Information -->
        <div class="space-y-8">
          <div class="card gradient-card border-none shadow-lg">
            <div class="p-8">
              <h3 class="font-serif text-2xl font-bold text-[#171940] mb-6">Informações de Contato</h3>

              <div class="space-y-6">
                <div class="flex items-start space-x-4">
                  <div class="w-12 h-12 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full flex items-center justify-center flex-shrink-0">
                    <MapPin class="w-6 h-6 text-white" />
                  </div>
                  <div>
                    <h4 class="font-semibold text-[#171940] mb-1">Endereço</h4>
                    <p class="text-[#404259]">
                      Av. Paulista, 1000 - Sala 1501<br />
                      Bela Vista, São Paulo - SP<br />
                      CEP: 01310-100
                    </p>
                  </div>
                </div>

                <div class="flex items-start space-x-4">
                  <div class="w-12 h-12 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full flex items-center justify-center flex-shrink-0">
                    <Phone class="w-6 h-6 text-white" />
                  </div>
                  <div>
                    <h4 class="font-semibold text-[#171940] mb-1">Telefone</h4>
                    <p class="text-[#404259]">
                      (11) 9999-9999<br />
                      (11) 3333-3333
                    </p>
                  </div>
                </div>

                <div class="flex items-start space-x-4">
                  <div class="w-12 h-12 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full flex items-center justify-center flex-shrink-0">
                    <Mail class="w-6 h-6 text-white" />
                  </div>
                  <div>
                    <h4 class="font-semibold text-[#171940] mb-1">E-mail</h4>
                    <p class="text-[#404259]">
                      contato@elloadvocacia.com.br<br />
                      helena@elloadvocacia.com.br
                    </p>
                  </div>
                </div>

                <div class="flex items-start space-x-4">
                  <div class="w-12 h-12 bg-gradient-to-br from-[#928FA6] to-[#171940] rounded-full flex items-center justify-center flex-shrink-0">
                    <Clock class="w-6 h-6 text-white" />
                  </div>
                  <div>
                    <h4 class="font-semibold text-[#171940] mb-1">Horário de Atendimento</h4>
                    <p class="text-[#404259]">
                      Segunda a Sexta: 8h às 18h<br />
                      Sábado: 8h às 12h
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="card gradient-card border-none shadow-lg">
  <div class="p-8">
    <h3 class="font-serif text-2xl font-bold text-[#171940] mb-6">
      Envie sua Mensagem
    </h3>

    <form @submit="handleSubmit" class="space-y-6">
      <!-- Nome -->
      <div>
        <input
          v-model="formData.name"
          type="text"
          placeholder="Seu nome completo"
          required
          class="w-full px-5 py-4 text-base border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-[#171940] focus:border-transparent transition-all duration-200"
        />
      </div>

      <!-- E-mail -->
      <div>
        <input
          v-model="formData.email"
          type="email"
          placeholder="Seu e-mail"
          required
          class="w-full px-5 py-4 text-base border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-[#171940] focus:border-transparent transition-all duration-200"
        />
      </div>

      <!-- Telefone -->
      <div>
        <input
          v-model="formData.phone"
          type="tel"
          placeholder="Seu telefone"
          required
          class="w-full px-5 py-4 text-base border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-[#171940] focus:border-transparent transition-all duration-200"
        />
      </div>

      <!-- Mensagem -->
      <div>
        <textarea
          v-model="formData.message"
          placeholder="Descreva seu caso ou dúvida"
          required
          rows="1"
          class="w-full px-5 py-4 text-base border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-[#171940] focus:border-transparent transition-all duration-200 resize-none"
        ></textarea>
      </div>

      <!-- Botão -->
      <button
        type="submit"
        class="w-full py-4 text-lg font-semibold text-white bg-[#171940] rounded-lg hover:bg-[#0f112e] transition-colors duration-200"
      >
        Enviar Mensagem
      </button>
    </form>
  </div>
</div>

      </div>
    </div>
  </section>

</template>

<script setup>
import { ref } from 'vue'
import { MapPin, Phone, Mail, Clock, CircleCheck} from 'lucide-vue-next'

const formData = ref({
  name: '',
  email: '',
  phone: '',
  message: '',
})

const handleSubmit = (e) => {
  e.preventDefault()
  alert('Mensagem enviada com sucesso! Entraremos em contato em breve.')
  formData.value = {
    name: '',
    email: '',
    phone: '',
    message: '',
  }
}
</script>
