<!-- pages/index.vue -->
<template>
  <div>
    <!-- Header Fixo -->
    <header class="fixed top-0 left-0 right-0 bg-white/95 backdrop-blur-md text-black z-50 border-b border-green-500/20">
      <nav class="container mx-auto px-4 py-4">
        <div class="flex justify-between items-center">
          <div class="flex items-center space-x-3">
            <div class="w-10 h-10 bg-white rounded-lg flex items-center justify-center font-bold text-xl border border-gray-200">
              <span class="text-black">G</span><span class="text-green-500">W</span>
            </div>
            <h1 class="text-2xl font-bold"><span class="text-black">GW</span> <span class="text-green-500">Fit Store</span></h1>
          </div>
          
          <!-- Menu Desktop -->
          <ul class="hidden lg:flex space-x-8 font-medium">
            <li><a href="#inicio" class="text-black hover:text-green-500 transition-colors">Início</a></li>
            <li><a href="#beneficios" class="text-black hover:text-green-500 transition-colors">Benefícios</a></li>
            <li><a href="#produtos" class="text-black hover:text-green-500 transition-colors">Produtos</a></li>
            <li><a href="#depoimentos" class="text-black hover:text-green-500 transition-colors">Depoimentos</a></li>
            <li><a href="#garantia" class="text-black hover:text-green-500 transition-colors">Garantia</a></li>
          </ul>
          
          <a href="https://wa.me/5586999313062?text=Olá! Gostaria de mais informações sobre os suplementos." class="bg-green-500 hover:bg-green-600 text-white px-6 py-2 rounded-lg font-semibold text-sm 
          transition-all transform hover:scale-105" target="_blank">Comprar Agora</a>

          <!-- Botão Menu Mobile -->
          <button @click="toggleMobileMenu" class="lg:hidden">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
        
        <!-- Menu Mobile -->
        <div v-show="mobileMenuOpen" class="lg:hidden mt-4 pb-4 border-t border-gray-700">
          <ul class="space-y-3 mt-4">
            <li><a href="#inicio" class="block hover:text-green-500" @click="closeMobileMenu">Início</a></li>
            <li><a href="#beneficios" class="block hover:text-green-500" @click="closeMobileMenu">Benefícios</a></li>
            <li><a href="#produtos" class="block hover:text-green-500" @click="closeMobileMenu">Produtos</a></li>
            <li><a href="#depoimentos" class="block hover:text-green-500" @click="closeMobileMenu">Depoimentos</a></li>
            <li><a href="#garantia" class="block hover:text-green-500" @click="closeMobileMenu">Garantia</a></li>
          </ul>
        </div>
      </nav>
    </header>

    <main>
      <!-- Hero Section -->
      <section id="inicio" class="relative min-h-screen bg-gradient-to-br from-black via-gray-900 to-green-900/20 text-white flex items-center overflow-hidden">
        <div class="absolute inset-0 bg-black/50"></div>
        <div class="absolute inset-0 bg-[url('/api/placeholder/1920/1080')] bg-cover bg-center opacity-30"></div>
        
        <div class="container mx-auto px-4 relative z-20 pt-20">
          <div class="grid lg:grid-cols-2 gap-12 items-center">
            <div class="space-y-8">
              <div class="space-y-4">
                <h2 class="text-5xl lg:text-7xl font-bold leading-tight">
                  TRANSFORME SEU 
                  <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-red-600">CORPO</span>
                </h2>
                <p class="text-2xl lg:text-3xl font-semibold text-gray-300">
                  Com os Melhores Suplementos do Brasil
                </p>
                <p class="text-lg text-gray-400 max-w-xl">
                  Alcance seus objetivos com suplementos de alta performance, testados e aprovados pela ANVISA. 
                  Resultados comprovados por milhares de atletas.
                </p>
              </div>
              
              <div class="flex flex-col sm:flex-row gap-4">
                <button @click="scrollToProducts" class="bg-gradient-to-r from-red-500 to-red-600 hover:from-red-600 hover:to-red-700 px-8 py-4 rounded-xl font-bold text-lg transition-all transform hover:scale-105 shadow-2xl">
                  🔥 GARANTA O SEU AGORA
                </button>
                <button @click="scrollToTestimonials" class="bg-white text-black hover:bg-gray-100 px-8 py-4 rounded-xl font-bold text-lg transition-all transform hover:scale-105 shadow-lg">
                  Ver Depoimentos
                </button>
              </div>
              
              <!-- Social Proof -->
              <div class="flex items-center space-x-6 text-sm">
                <div class="flex items-center space-x-2">
                  <div class="flex -space-x-2">
                    <!-- <img src="/api/placeholder/32/32" alt="Cliente satisfeito" class="w-8 h-8 rounded-full border-2 border-white">
                    <img src="/api/placeholder/32/32" alt="Cliente satisfeito" class="w-8 h-8 rounded-full border-2 border-white">
                    <img src="/api/placeholder/32/32" alt="Cliente satisfeito" class="w-8 h-8 rounded-full border-2 border-white"> -->
                  </div>
                </div>
                <div class="flex items-center space-x-1">
                  <div class="flex text-yellow-400">
                    ⭐⭐⭐⭐⭐
                  </div>
                  <span class="text-gray-300">4.9/5</span>
                </div>
              </div>
            </div>
            
            <div class="relative">
              <!-- <img src="/api/placeholder/600/700" 
                   alt="Atleta com físico definido segurando produtos G-Suplements" 
                   class="w-full max-w-md mx-auto rounded-2xl shadow-2xl"> -->
              <div class="absolute -top-4 -right-4 bg-yellow-400 text-black px-4 py-2 rounded-lg font-bold text-sm rotate-12">
                🏆 #1 EM VENDAS
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Benefícios -->
      <section id="beneficios" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl lg:text-5xl font-bold text-gray-800 mb-4">
              Por que Escolher a GW Fit Store?
            </h2>
            <p class="text-xl text-gray-600 max-w-3xl mx-auto">
              Somos a marca de suplementos mais confiável do Brasil, com produtos de alta qualidade e resultados comprovados
            </p>
          </div>
          
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all transform hover:-translate-y-2">
              <div class="w-16 h-16 bg-gradient-to-r from-green-400 to-green-500 rounded-2xl flex items-center justify-center mb-6">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                </svg>
              </div>
              <h3 class="text-xl font-bold text-gray-800 mb-3">Aprovado pela ANVISA</h3>
              <p class="text-gray-600">Todos os nossos suplementos são testados e aprovados pelos órgãos competentes</p>
            </div>
            
            <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all transform hover:-translate-y-2">
              <div class="w-16 h-16 bg-gradient-to-r from-blue-400 to-blue-500 rounded-2xl flex items-center justify-center mb-6">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                </svg>
              </div>
              <h3 class="text-xl font-bold text-gray-800 mb-3">Resultados Rápidos</h3>
              <p class="text-gray-600">Fórmulas cientificamente desenvolvidas para máxima absorção e eficácia</p>
            </div>
            
            <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all transform hover:-translate-y-2">
              <div class="w-16 h-16 bg-gradient-to-r from-purple-400 to-purple-500 rounded-2xl flex items-center justify-center mb-6">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4"></path>
                </svg>
              </div>
              <h3 class="text-xl font-bold text-gray-800 mb-3">Frete Grátis</h3>
              <p class="text-gray-600">Entrega gratuita para todo o Brasil em compras acima de R$ 99</p>
            </div>
            
            <div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all transform hover:-translate-y-2">
              <div class="w-16 h-16 bg-gradient-to-r from-red-400 to-red-500 rounded-2xl flex items-center justify-center mb-6">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1"></path>
                </svg>
              </div>
              <h3 class="text-xl font-bold text-gray-800 mb-3">Melhor Preço</h3>
              <p class="text-gray-600">Garantimos o melhor preço do mercado com qualidade premium</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Produtos em Destaque -->
      <section id="produtos" class="py-20 bg-black text-white">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl lg:text-5xl font-bold mb-4">
              Produtos <span class="text-red-500">em Destaque</span>
            </h2>
            <p class="text-xl text-gray-300 max-w-3xl mx-auto">
              Os suplementos mais vendidos do Brasil. Escolhidos por atletas profissionais e amadores
            </p>
          </div>
          
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div v-for="product in products" :key="product.id" 
                 class="bg-gradient-to-b from-gray-900 to-gray-800 p-8 rounded-2xl shadow-2xl hover:transform hover:-translate-y-4 transition-all duration-300 border border-gray-700">
              <div class="relative mb-6">
                <!-- <img :src="product.image" 
                     :alt="`${product.name} - suplemento de alta qualidade G-Suplements`" 
                     class="w-full h-64 object-cover rounded-xl"> -->
                <div class="absolute top-4 left-4 bg-red-500 text-white px-3 py-1 rounded-full text-sm font-bold">
                  {{ product.discount }}
                </div>
                <div class="absolute top-4 right-4 bg-yellow-400 text-black px-2 py-1 rounded text-xs font-bold">
                  BESTSELLER
                </div>
              </div>
              
              <div class="space-y-4">
                <h3 class="text-2xl font-bold text-white">{{ product.name }}</h3>
                <p class="text-gray-400">{{ product.description }}</p>
                
                <ul class="space-y-2">
                  <li v-for="benefit in product.benefits" :key="benefit" class="flex items-center text-sm text-gray-300">
                    <span class="text-green-400 mr-2">✓</span>
                    {{ benefit }}
                  </li>
                </ul>
                
                <div class="flex items-center space-x-3">
                  <span class="text-3xl font-bold text-red-500">{{ product.price }}</span>
                  <span class="text-lg text-gray-500 line-through">{{ product.originalPrice }}</span>
                </div>
                
                <button class="w-full bg-gradient-to-r from-red-500 to-red-600 hover:from-red-600 hover:to-red-700 py-4 rounded-xl font-bold text-lg transition-all transform hover:scale-105 shadow-lg">
                  🛒 COMPRAR AGORA
                </button>
                
                <p class="text-center text-xs text-gray-400">
                  ou em até 12x de {{ (parseFloat(product.price.replace('R$ ', '').replace(',', '.')) / 12).toFixed(2).replace('.', ',') }} sem juros
                </p>
              </div>
            </div>
          </div>
          
          <div class="text-center mt-12">
          </div>
        </div>
      </section>

      <!-- Depoimentos -->
      <section id="depoimentos" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl lg:text-5xl font-bold text-gray-800 mb-4">
              O Que Nossos <span class="text-red-500">Clientes</span> Dizem
            </h2>
          </div>
          
          <div class="grid md:grid-cols-3 gap-8">
            <div v-for="testimonial in testimonials" :key="testimonial.id"
                 class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-2xl transition-all">
              <div class="flex text-yellow-400 text-xl mb-4">
                ⭐⭐⭐⭐⭐
              </div>
              <p class="text-gray-700 mb-6 italic">"{{ testimonial.comment }}"</p>
              <div class="flex items-center space-x-4">
                <div>
                  <h4 class="font-bold text-gray-800">{{ testimonial.name }}</h4>
                  <p class="text-gray-500 text-sm">{{ testimonial.location }}</p>
                  <p class="text-red-500 text-sm font-semibold">{{ testimonial.result }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Garantia -->
      <section id="garantia" class="py-20 bg-gradient-to-r from-green-600 to-green-700 text-white">
        <div class="container mx-auto px-4 text-center">
          <div class="max-w-4xl mx-auto">
            <div class="w-24 h-24 bg-white rounded-full flex items-center justify-center mx-auto mb-8">
              <svg class="w-12 h-12 text-green-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
              </svg>
            </div>
            
            <h2 class="text-4xl lg:text-5xl font-bold mb-6">
              Garantia de 30 Dias
            </h2>
            <p class="text-2xl mb-8">
              Satisfação Garantida ou seu Dinheiro de Volta!
            </p>
            <p class="text-lg mb-8 max-w-2xl mx-auto">
              Estamos tão confiantes na qualidade dos nossos produtos que oferecemos 30 dias de garantia incondicional. 
              Se não ficar 100% satisfeito, devolvemos seu dinheiro sem perguntas.
            </p>
            
            <div class="grid md:grid-cols-3 gap-8 mt-12">
              <div class="text-center">
                <div class="w-16 h-16 bg-white/20 rounded-full flex items-center justify-center mx-auto mb-4">
                  <span class="text-2xl">📦</span>
                </div>
                <h3 class="font-bold text-xl mb-2">Compre com Confiança</h3>
                <p>Produto original com nota fiscal e garantia</p>
              </div>
              
              <div class="text-center">
                <div class="w-16 h-16 bg-white/20 rounded-full flex items-center justify-center mx-auto mb-4">
                  <span class="text-2xl">🔄</span>
                </div>
                <h3 class="font-bold text-xl mb-2">Troca Fácil</h3>
                <p>Processo simples e rápido para trocas e devoluções</p>
              </div>
              
              <div class="text-center">
                <div class="w-16 h-16 bg-white/20 rounded-full flex items-center justify-center mx-auto mb-4">
                  <span class="text-2xl">💰</span>
                </div>
                <h3 class="font-bold text-xl mb-2">Reembolso Total</h3>
                <p>Dinheiro de volta em até 7 dias úteis</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- FAQ -->
      <section class="py-20 bg-white">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl lg:text-5xl font-bold text-gray-800 mb-4">
              Perguntas Frequentes
            </h2>
            <p class="text-xl text-gray-600">Tire suas dúvidas sobre nossos produtos e serviços</p>
          </div>
          
          <div class="max-w-3xl mx-auto space-y-4">
            <div v-for="(faq, index) in faqs" :key="index" class="border border-gray-200 rounded-xl">
              <button @click="toggleFaq(index)" 
                      class="w-full px-6 py-4 text-left font-semibold text-gray-800 hover:bg-gray-50 flex justify-between items-center">
                {{ faq.question }}
                <svg class="w-5 h-5 transition-transform" :class="{'rotate-180': faqOpen[index]}" 
                     fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="faqOpen[index]" class="px-6 pb-4 text-gray-600">
                {{ faq.answer }}
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Contato/Suporte -->
      <section class="py-20 bg-gray-900 text-white">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl lg:text-5xl font-bold mb-4">
              Suporte e <span class="text-red-500">Atendimento</span>
            </h2>
            <p class="text-xl text-gray-300">Estamos aqui para ajudar você a alcançar seus objetivos</p>
          </div>
          
          <div class="grid md:grid-cols-4 gap-8">
            <div class="text-center">
              <div class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
                </svg>
              </div>
              <h3 class="font-bold text-xl mb-2">WhatsApp</h3>
              <p class="text-gray-300 mb-4">+55 (86) 999313062</p>
              <p class="text-sm text-gray-400">Resposta em até 5 minutos</p>
            </div>
            
            <div class="text-center">
              <div class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                </svg>
              </div>
              <h3 class="font-bold text-xl mb-2">E-mail</h3>
              <p class="text-gray-300 mb-4">contato@gwfitstore.com</p>
              <p class="text-sm text-gray-400">Resposta em até 2 horas</p>
            </div>
            
            <div class="text-center">
              <div class="w-16 h-16 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full flex items-center justify-center mx-auto mb-4">
                <span class="text-2xl">📷</span>
              </div>
              <h3 class="font-bold text-xl mb-2">Instagram</h3>
              <p class="text-gray-300 mb-4">@g_suplements</p>
              <p class="text-sm text-gray-400">Dicas e novidades diárias</p>
            </div>
            
            <div class="text-center">
              <div class="w-16 h-16 bg-yellow-500 rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                </svg>
              </div>
              <h3 class="font-bold text-xl mb-2">Horário</h3>
              <p class="text-gray-300 mb-4">8h às 22h</p>
              <p class="text-sm text-gray-400">Segunda a sábado</p>
            </div>
          </div>
        </div>
      </section>

      <!-- CTA Final -->
      <section class="py-20 bg-gradient-to-r from-green-600 to-green-700 text-white">
        <div class="container mx-auto px-4 text-center">
          <div class="max-w-4xl mx-auto">
            <h2 class="text-4xl lg:text-6xl font-bold mb-6">
              Não Perca Esta Oportunidade!
            </h2>
            <p class="text-2xl mb-8">
              Transforme seu corpo com os melhores suplementos do Brasil
            </p>
            <p class="text-lg mb-8 max-w-2xl mx-auto">
              Milhares de pessoas já alcançaram seus objetivos com nossos produtos. 
              Chegou a sua vez de ter o corpo dos seus sonhos.
            </p>
            
            <div class="bg-white/10 backdrop-blur-md rounded-2xl p-8 mb-8 inline-block">
              <p class="text-2xl font-bold mb-2">⏰ OFERTA LIMITADA</p>
              <p class="text-lg">Esta promoção acaba em:</p>
              <div class="text-4xl font-bold mt-4">
                {{ formatTime(timeLeft.hours) }}:{{ formatTime(timeLeft.minutes) }}:{{ formatTime(timeLeft.seconds) }}
              </div>
            </div>
            
            <div class="space-y-4">
              <button class="bg-yellow-400 hover:bg-yellow-300 text-black px-12 py-6 rounded-2xl font-bold text-2xl transition-all transform hover:scale-105 shadow-2xl">
                🔥 COMPRAR AGORA COM DESCONTO
              </button>
              <p class="text-lg">✅ Frete Grátis | ✅ Garantia de 30 dias | ✅ Parcelamento sem juros</p>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="bg-white text-black py-16">
      <div class="container mx-auto px-4">
        <div class="flex items-center space-x-3 mb-6">
          <div class="w-12 h-12 bg-white rounded-lg flex items-center justify-center font-bold text-xl border border-gray-200">
            <span class="text-black">G</span><span class="text-green-500">W</span>
          </div>
          <h3 class="text-2xl font-bold"><span class="text-black">GW</span> <span class="text-green-500">Fit Store</span></h3>
        </div>
        <p class="text-gray-400 mb-6">
          Os melhores suplementos alimentares do Brasil. Qualidade premium, 
          resultados garantidos e preços imbatíveis.
        </p>
        <div class="flex space-x-4 mb-8">
          <a href="https://instagram.com/g_suplements" target="_blank" rel="noopener" 
             class="w-10 h-10 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center hover:scale-110 transition-transform">
            <span class="text-sm">📷</span>
          </a>
          <a href="https://facebook.com/g.suplements" target="_blank" rel="noopener"
             class="w-10 h-10 bg-blue-600 rounded-lg flex items-center justify-center hover:scale-110 transition-transform">
            <span class="text-sm">f</span>
          </a>
          <a href="https://wa.me/5511999999999" target="_blank" rel="noopener"
             class="w-10 h-10 bg-green-500 rounded-lg flex items-center justify-center hover:scale-110 transition-transform">
            <span class="text-sm">💬</span>
          </a>
        </div>
        
        <div class="grid md:grid-cols-4 gap-8">
          <div>
            <h4 class="text-lg font-bold mb-6">Produtos</h4>
            <ul class="space-y-3 text-gray-400">
              <li><NuxtLink to="/produtos/whey-protein" class="hover:text-red-400 transition-colors">Whey Protein</NuxtLink></li>
              <li><NuxtLink to="/produtos/creatina" class="hover:text-red-400 transition-colors">Creatina</NuxtLink></li>
              <li><NuxtLink to="/produtos/pre-treino" class="hover:text-red-400 transition-colors">Pré-treino</NuxtLink></li>
              <li><NuxtLink to="/produtos/termogenico" class="hover:text-red-400 transition-colors">Termogênico</NuxtLink></li>
              <li><NuxtLink to="/produtos/multivitaminico" class="hover:text-red-400 transition-colors">Multivitamínico</NuxtLink></li>
              <li><NuxtLink to="/produtos" class="hover:text-red-400 transition-colors">Ver Todos</NuxtLink></li>
            </ul>
          </div>
          
          <div>
            <h4 class="text-lg font-bold mb-6">Empresa</h4>
            <ul class="space-y-3 text-gray-400">
              <li><NuxtLink to="/sobre" class="hover:text-red-400 transition-colors">Sobre Nós</NuxtLink></li>
              <li><NuxtLink to="/contato" class="hover:text-red-400 transition-colors">Contato</NuxtLink></li>
              <li><NuxtLink to="/blog" class="hover:text-red-400 transition-colors">Blog</NuxtLink></li>
              <li><NuxtLink to="/afiliados" class="hover:text-red-400 transition-colors">Programa de Afiliados</NuxtLink></li>
              <li><NuxtLink to="/trabalhe-conosco" class="hover:text-red-400 transition-colors">Trabalhe Conosco</NuxtLink></li>
            </ul>
          </div>
          
          <div>
            <h4 class="text-lg font-bold mb-6">Suporte</h4>
            <ul class="space-y-3 text-gray-400">
              <li><NuxtLink to="/faq" class="hover:text-red-400 transition-colors">Perguntas Frequentes</NuxtLink></li>
              <li><NuxtLink to="/politica-privacidade" class="hover:text-red-400 transition-colors">Política de Privacidade</NuxtLink></li>
              <li><NuxtLink to="/termos-uso" class="hover:text-red-400 transition-colors">Termos de Uso</NuxtLink></li>
              <li><NuxtLink to="/politica-entrega" class="hover:text-red-400 transition-colors">Política de Entrega</NuxtLink></li>
              <li><NuxtLink to="/trocas-devolucoes" class="hover:text-red-400 transition-colors">Trocas e Devoluções</NuxtLink></li>
            </ul>
          </div>
        </div>
        
        <hr class="border-gray-800 my-12">
        
        <div class="grid md:grid-cols-2 gap-8">
          <div>
            <h4 class="font-bold text-lg mb-4">Informações Legais</h4>
            <div class="text-gray-400 text-sm space-y-2">
              <p><strong>GW Fit Store</strong></p>
              <p>Telefone: +55 (86) 99313-062</p>
              <p>E-mail: contato@gwfitstore.com.br</p>
            </div>
          </div>
        </div>
        
        <hr class="border-gray-800 my-8">
        
        <div class="flex flex-col md:flex-row justify-between items-center text-gray-400 text-sm">
          <p>© 2025 GW Fit Store. Todos os direitos reservados.</p>
          <p class="mt-2 md:mt-0">
            Desenvolvido com ❤️ para transformar vidas através do fitness
          </p>
        </div>
      </div>
    </footer>

    <!-- WhatsApp Float Button -->
    <a href="https://wa.me/5586999313062?text=Olá! Gostaria de mais informações sobre os suplementos."
       target="_blank" rel="noopener"
       class="fixed bottom-6 right-6 w-14 h-14 bg-green-500 hover:bg-green-600 rounded-full flex items-center justify-center shadow-2xl z-50 transition-all transform hover:scale-110">
      <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/>
      </svg>
    </a>
  </div>
</template>

<script setup>
// SEO Configuration
useHead({
  title: 'GW Fit Store | Suplementos de Alta Performance para Corpo e Mente | Compre Online',
  meta: [
    { name: 'description', content: 'Compre suplementos da GW Fit Store e alcance seus resultados com qualidade e segurança. Whey Protein, Creatina, Pré-treino e muito mais. Frete grátis para todo Brasil!' },
    { name: 'keywords', content: 'suplementos alimentares, comprar suplementos online, whey protein, creatina, GW Fit Store, suplementos brasil, loja suplementos, proteína, termogênico, pré-treino' },
    { name: 'author', content: 'GW Fit Store' },
    { property: 'og:title', content: 'GW Fit Store | Os Melhores Suplementos do Brasil' },
    { property: 'og:site_name', content: 'GW Fit Store' },
    { name: 'twitter:title', content: 'GW Fit Store | Suplementos de Alta Performance' },
  ],
  link: [
    { rel: 'canonical', href: 'https://gwfitstore.com.br' },
  ]
});

// Structured Data (Schema.org)
// useJsonld([
//   {
//     '@context': 'https://schema.org',
//     '@type': 'Organization',
//     'name': 'G-Suplements',
//     'url': 'https://g-suplements.com.br',
//     'logo': 'https://g-suplements.com.br/logo.png',
//     'description': 'Loja online de suplementos alimentares de alta qualidade',
//     'address': {
//       '@type': 'PostalAddress',
//       'streetAddress': 'Rua dos Suplementos, 123',
//       'addressLocality': 'São Paulo',
//       'addressRegion': 'SP',
//       'postalCode': '01234-567',
//       'addressCountry': 'BR'
//     },
//     'contactPoint': {
//       '@type': 'ContactPoint',
//       'telephone': '+55-11-99999-9999',
//       'contactType': 'customer service'
//     },
//     'sameAs': [
//       'https://instagram.com/g_suplements',
//       'https://facebook.com/g.suplements'
//     ]
//   },
//   {
//     '@context': 'https://schema.org',
//     '@type': 'WebSite',
//     'name': 'G-Suplements',
//     'url': 'https://g-suplements.com.br',
//     'potentialAction': {
//       '@type': 'SearchAction',
//       'target': 'https://g-suplements.com.br/buscar?q={search_term_string}',
//       'query-input': 'required name=search_term_string'
//     }
//   }
// ]);

// Reactive Data
const mobileMenuOpen = ref(false);
const timeLeft = ref({
  hours: 23,
  minutes: 59,
  seconds: 59
});

const faqOpen = ref({});

const products = ref([
  {
    id: 1,
    name: "Whey Protein Premium",
    description: "Proteína isolada com 25g por dose, absorção rápida e sabor incrível",
    price: "R$ 89,90",
    originalPrice: "R$ 129,90",
    image: "/api/placeholder/400/400",
    discount: "31% OFF",
    benefits: ["25g de proteína por dose", "Absorção rápida", "Sem lactose", "Diversos sabores"]
  },
  {
    id: 2,
    name: "Creatina Monohidratada",
    description: "100% pura, micronizada para melhor dissolução e absorção",
    price: "R$ 49,90",
    originalPrice: "R$ 69,90",
    image: "/api/placeholder/400/400",
    discount: "29% OFF",
    benefits: ["100% pura", "Micronizada", "Sem sabor", "300g"]
  },
  {
    id: 3,
    name: "Pré-Treino Explosion",
    description: "Fórmula avançada com cafeína, arginina e beta-alanina",
    price: "R$ 79,90",
    originalPrice: "R$ 109,90",
    image: "/api/placeholder/400/400",
    discount: "27% OFF",
    benefits: ["Energia explosiva", "Foco mental", "Pump muscular", "200mg cafeína"]
  },
  {
    id: 4,
    name: "Termogênico Fire",
    description: "Queimador de gordura com ingredientes naturais e termogênicos",
    price: "R$ 69,90",
    originalPrice: "R$ 99,90",
    image: "/api/placeholder/400/400",
    discount: "30% OFF",
    benefits: ["Queima gordura", "Acelera metabolismo", "Ingredientes naturais", "60 cápsulas"]
  },
  {
    id: 5,
    name: "Multivitamínico Complete",
    description: "Complexo vitamínico completo para saúde e performance",
    price: "R$ 39,90",
    originalPrice: "R$ 59,90",
    image: "/api/placeholder/400/400",
    discount: "33% OFF",
    benefits: ["26 vitaminas e minerais", "Imunidade", "Energia", "60 comprimidos"]
  }
]);

const testimonials = ref([
  {
    id: 1,
    name: "Carlos Silva",
    location: "São Paulo, SP",
    result: "Perdeu 15kg em 3 meses",
    comment: "Produtos de excelente qualidade! O whey protein tem um sabor incrível e os resultados apareceram rapidamente. Recomendo para todos os meus amigos da academia.",
    photo: "/api/placeholder/80/80"
  },
  {
    id: 2,
    name: "Marina Santos",
    location: "Rio de Janeiro, RJ",
    result: "Ganhou 8kg de massa magra",
    comment: "Uso os suplementos da GW Fit Store há 6 meses e nunca vi resultados tão rápidos. A creatina é pura e o atendimento é excepcional!",
    photo: "/api/placeholder/80/80"
  },
  {
    id: 3,
    name: "Roberto Lima",
    location: "Belo Horizonte, MG",
    result: "Melhorou performance em 40%",
    comment: "O pré-treino Explosion mudou completamente meus treinos. Mais energia, foco e disposição. Não treino mais sem ele!",
    photo: "/api/placeholder/80/80"
  }
]);

const faqs = ref([
  {
    question: "Os produtos são originais e certificados?",
    answer: "Sim! Todos os nossos suplementos são 100% originais, testados em laboratório e aprovados pela ANVISA. Trabalhamos apenas com marcas renomadas e fornecedores certificados."
  },
  {
    question: "Qual o prazo de entrega?",
    answer: "O prazo varia conforme a região: Sudeste (2-4 dias úteis), Sul (3-5 dias úteis), Nordeste (4-6 dias úteis), Norte/Centro-Oeste (5-8 dias úteis). Frete grátis para compras acima de R$ 99."
  },
  {
    question: "Como funciona a garantia?",
    answer: "Oferecemos 30 dias de garantia incondicional. Se não ficar satisfeito com o produto, devolvemos 100% do seu dinheiro sem perguntas."
  },
  {
    question: "Posso parcelar minha compra?",
    answer: "Sim! Aceitamos cartão de crédito em até 12x sem juros, PIX com 5% de desconto, boleto bancário e PicPay."
  },
  {
    question: "Os suplementos têm contraindicação?",
    answer: "Nossos produtos são seguros quando utilizados conforme as instruções. Recomendamos consultar um médico ou nutricionista antes de iniciar qualquer suplementação."
  },
  {
    question: "Como acompanhar meu pedido?",
    answer: "Após a confirmação do pagamento, você recebe um código de rastreamento por e-mail e WhatsApp para acompanhar sua entrega em tempo real."
  }
]);

// Methods
const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};

const closeMobileMenu = () => {
  mobileMenuOpen.value = false;
};

const scrollToProducts = () => {
  const element = document.getElementById('produtos');
  element?.scrollIntoView({ behavior: 'smooth' });
};
const scrollToTestimonials = () => {
  const element = document.getElementById('depoimentos');
  element?.scrollIntoView({ behavior: 'smooth' });
};

const toggleFaq = (index) => {
  faqOpen.value = {
    ...faqOpen.value,
    [index]: !faqOpen.value[index]
  };
};

const formatTime = (time) => {
  return time.toString().padStart(2, '0');
};

// Timer countdown
onMounted(() => {
  const timer = setInterval(() => {
    timeLeft.value = {
      ...timeLeft.value,
      seconds: timeLeft.value.seconds > 0 ? timeLeft.value.seconds - 1 : 59,
      minutes: timeLeft.value.seconds === 0 && timeLeft.value.minutes > 0 ? timeLeft.value.minutes - 1 : timeLeft.value.minutes,
      hours: timeLeft.value.minutes === 0 && timeLeft.value.seconds === 0 && timeLeft.value.hours > 0 ? timeLeft.value.hours - 1 : timeLeft.value.hours
    };
    
    if (timeLeft.value.hours === 0 && timeLeft.value.minutes === 0 && timeLeft.value.seconds === 0) {
      timeLeft.value = { hours: 23, minutes: 59, seconds: 59 };
    }
  }, 1000);
  
  onBeforeUnmount(() => {
    clearInterval(timer);
  });
});
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}

.animate-pulse {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}
</style>