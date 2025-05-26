<template>
  <div class="min-h-screen bg-black text-white overflow-x-hidden">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-black/80 backdrop-blur-xl border-b border-gray-800/50 z-50 transition-all duration-300">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
          <div class="flex items-center">
            <div class="flex-shrink-0 flex items-center group">
              <div class="w-8 h-8 bg-gradient-to-r from-blue-500 to-purple-600 rounded-lg flex items-center justify-center transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12">
                <span class="text-white font-bold text-sm">S</span>
              </div>
              <span class="ml-2 text-xl font-bold text-white transition-colors duration-300 group-hover:text-blue-400">SaaSify</span>
            </div>
          </div>
          
          <!-- Desktop Navigation -->
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-8">
              <a href="#features" class="text-gray-400 hover:text-white px-3 py-2 text-sm font-medium transition-all duration-300 hover:scale-105 relative group">
                Features
                <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-purple-600 transition-all duration-300 group-hover:w-full"></span>
              </a>
              <a href="#pricing" class="text-gray-400 hover:text-white px-3 py-2 text-sm font-medium transition-all duration-300 hover:scale-105 relative group">
                Pricing
                <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-purple-600 transition-all duration-300 group-hover:w-full"></span>
              </a>
              <a href="#reviews" class="text-gray-400 hover:text-white px-3 py-2 text-sm font-medium transition-all duration-300 hover:scale-105 relative group">
                Reviews
                <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-purple-600 transition-all duration-300 group-hover:w-full"></span>
              </a>
              <a href="#faq" class="text-gray-400 hover:text-white px-3 py-2 text-sm font-medium transition-all duration-300 hover:scale-105 relative group">
                FAQ
                <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-purple-600 transition-all duration-300 group-hover:w-full"></span>
              </a>
            </div>
          </div>
          
          <div class="hidden md:flex items-center space-x-4">
            <button class="text-gray-400 hover:text-white px-4 py-2 text-sm font-medium transition-all duration-300 hover:scale-105">
              Sign In
            </button>
            <button class="bg-gradient-to-r from-blue-500 to-purple-600 text-white px-6 py-2 rounded-lg text-sm font-medium hover:from-blue-600 hover:to-purple-700 transition-all duration-300 transform hover:scale-105 hover:shadow-lg hover:shadow-blue-500/25 relative overflow-hidden group">
              <span class="relative z-10">Get Started</span>
              <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-blue-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </button>
          </div>
          
          <!-- Mobile menu button -->
          <div class="md:hidden">
            <button @click="mobileMenuOpen = !mobileMenuOpen" class="text-gray-400 hover:text-white p-2 transition-all duration-300 hover:scale-110">
              <svg class="h-6 w-6 transition-transform duration-300" :class="{ 'rotate-90': mobileMenuOpen }" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>
      </div>
      
      <!-- Mobile Navigation -->
      <transition
        enter-active-class="transition duration-300 ease-out"
        enter-from-class="transform -translate-y-full opacity-0"
        enter-to-class="transform translate-y-0 opacity-100"
        leave-active-class="transition duration-200 ease-in"
        leave-from-class="transform translate-y-0 opacity-100"
        leave-to-class="transform -translate-y-full opacity-0"
      >
        <div v-if="mobileMenuOpen" class="md:hidden bg-black/95 backdrop-blur-xl border-t border-gray-800/50">
          <div class="px-2 pt-2 pb-3 space-y-1">
            <a href="#features" class="block px-3 py-2 text-base font-medium text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Features</a>
            <a href="#pricing" class="block px-3 py-2 text-base font-medium text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Pricing</a>
            <a href="#reviews" class="block px-3 py-2 text-base font-medium text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Reviews</a>
            <a href="#faq" class="block px-3 py-2 text-base font-medium text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">FAQ</a>
            <div class="pt-4 pb-2 border-t border-gray-800/50">
              <button class="block w-full text-left px-3 py-2 text-base font-medium text-gray-400 hover:text-white transition-all duration-300">
                Sign In
              </button>
              <button class="block w-full mt-2 bg-gradient-to-r from-blue-500 to-purple-600 text-white px-3 py-2 rounded-lg text-base font-medium transition-all duration-300 hover:scale-105">
                Get Started
              </button>
            </div>
          </div>
        </div>
      </transition>
    </nav>

    <!-- Hero Section -->
    <section class="pt-20 pb-16 sm:pt-24 sm:pb-20 lg:pt-32 lg:pb-28 relative overflow-hidden">
      <!-- Animated background elements -->
      <div class="absolute inset-0 overflow-hidden">
        <div class="absolute -top-40 -right-40 w-80 h-80 bg-gradient-to-r from-blue-500/20 to-purple-600/20 rounded-full blur-3xl animate-pulse"></div>
        <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-gradient-to-r from-purple-600/20 to-blue-500/20 rounded-full blur-3xl animate-pulse" style="animation-delay: 2s;"></div>
      </div>
      
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        <div class="text-center">
          <div class="animate-fade-in-up" style="animation-delay: 0.1s;">
            <h1 class="text-4xl sm:text-5xl lg:text-7xl font-bold text-white leading-tight">
              Build Your SaaS
              <span class="bg-gradient-to-r from-blue-400 via-purple-500 to-blue-600 bg-clip-text text-transparent animate-gradient-x">
                Faster Than Ever
              </span>
            </h1>
          </div>
          <div class="animate-fade-in-up" style="animation-delay: 0.3s;">
            <p class="mt-6 text-lg sm:text-xl text-gray-300 max-w-3xl mx-auto leading-relaxed">
              The complete platform for modern SaaS applications. Ship faster, scale effortlessly, and focus on what matters most - your customers.
            </p>
          </div>
          <div class="mt-10 flex flex-col sm:flex-row gap-4 justify-center animate-fade-in-up" style="animation-delay: 0.5s;">
            <button class="bg-gradient-to-r from-blue-500 to-purple-600 text-white px-8 py-4 rounded-lg text-lg font-semibold hover:from-blue-600 hover:to-purple-700 transition-all duration-300 transform hover:scale-105 hover:shadow-2xl hover:shadow-blue-500/25 relative overflow-hidden group">
              <span class="relative z-10">Start Free Trial</span>
              <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-blue-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </button>
            <button class="border-2 border-gray-700 text-gray-300 px-8 py-4 rounded-lg text-lg font-semibold hover:border-gray-500 hover:bg-gray-900/50 hover:text-white transition-all duration-300 transform hover:scale-105 backdrop-blur-sm">
              Watch Demo
            </button>
          </div>
          <div class="mt-12 animate-fade-in-up" style="animation-delay: 0.7s;">
            <div class="relative max-w-4xl mx-auto group">
              <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-purple-600 rounded-2xl blur-3xl opacity-30 group-hover:opacity-50 transition-opacity duration-500"></div>
              <div class="relative bg-gray-900/50 rounded-2xl shadow-2xl border border-gray-800/50 p-2 backdrop-blur-xl hover:border-gray-700/50 transition-all duration-500">
                <PlaceholderImage :width="800" :height="400" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-16 sm:py-20 lg:py-24 bg-gray-950/50 relative">
      <div class="absolute inset-0 bg-gradient-to-b from-transparent via-gray-950/20 to-transparent"></div>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        <div class="text-center mb-16">
          <div class="animate-fade-in-up">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
              Everything You Need to Scale
            </h2>
            <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
              Powerful features designed to help you build, launch, and grow your SaaS business with confidence.
            </p>
          </div>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="(feature, index) in features" :key="feature.title" 
               class="bg-gray-900/50 rounded-xl p-8 shadow-2xl hover:shadow-blue-500/10 transition-all duration-500 transform hover:scale-105 hover:-translate-y-2 border border-gray-800/50 hover:border-gray-700/50 backdrop-blur-sm group animate-fade-in-up"
               :style="{ animationDelay: `${index * 0.1}s` }">
            <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-purple-600 rounded-lg flex items-center justify-center mb-6 transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12">
              <span class="text-white text-xl">{{ feature.icon }}</span>
            </div>
            <h3 class="text-xl font-semibold text-white mb-4 group-hover:text-blue-400 transition-colors duration-300">{{ feature.title }}</h3>
            <p class="text-gray-400 leading-relaxed group-hover:text-gray-300 transition-colors duration-300">{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="py-16 sm:py-20 lg:py-24 relative">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="(stat, index) in stats" :key="stat.label" 
               class="text-center group animate-fade-in-up"
               :style="{ animationDelay: `${index * 0.2}s` }">
            <div class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-2 transition-all duration-300 group-hover:scale-110 group-hover:text-blue-400">
              {{ stat.value }}
            </div>
            <div class="text-gray-400 text-sm sm:text-base group-hover:text-gray-300 transition-colors duration-300">{{ stat.label }}</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="py-16 sm:py-20 lg:py-24 bg-gray-950/50 relative">
      <div class="absolute inset-0 bg-gradient-to-b from-transparent via-gray-950/20 to-transparent"></div>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        <div class="text-center mb-16">
          <div class="animate-fade-in-up">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
              Simple, Transparent Pricing
            </h2>
            <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
              Choose the perfect plan for your business. No hidden fees, no surprises.
            </p>
          </div>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 max-w-5xl mx-auto">
          <div v-for="(plan, index) in pricingPlans" :key="plan.name" 
               :class="[
                 'bg-gray-900/50 rounded-2xl p-8 shadow-2xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-2 border backdrop-blur-sm group animate-fade-in-up',
                 plan.popular ? 'ring-2 ring-blue-500/50 relative border-blue-500/50 hover:ring-blue-400/70' : 'border-gray-800/50 hover:border-gray-700/50'
               ]"
               :style="{ animationDelay: `${index * 0.2}s` }">
            <div v-if="plan.popular" class="absolute -top-4 left-1/2 transform -translate-x-1/2">
              <span class="bg-gradient-to-r from-blue-500 to-purple-600 text-white px-4 py-2 rounded-full text-sm font-medium animate-pulse">
                Most Popular
              </span>
            </div>
            <div class="text-center">
              <h3 class="text-2xl font-bold text-white mb-4 group-hover:text-blue-400 transition-colors duration-300">{{ plan.name }}</h3>
              <div class="mb-6">
                <span class="text-4xl sm:text-5xl font-bold text-white group-hover:scale-110 transition-transform duration-300 inline-block">${{ plan.price }}</span>
                <span class="text-gray-400">/month</span>
              </div>
              <ul class="space-y-4 mb-8">
                <li v-for="(feature, featureIndex) in plan.features" :key="feature" 
                    class="flex items-center animate-fade-in-up"
                    :style="{ animationDelay: `${(index * 0.2) + (featureIndex * 0.1)}s` }">
                  <svg class="w-5 h-5 text-green-400 mr-3 transition-transform duration-300 group-hover:scale-110" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                  </svg>
                  <span class="text-gray-400 group-hover:text-gray-300 transition-colors duration-300">{{ feature }}</span>
                </li>
              </ul>
              <button :class="[
                'w-full py-3 px-6 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 relative overflow-hidden group',
                plan.popular 
                  ? 'bg-gradient-to-r from-blue-500 to-purple-600 text-white hover:from-blue-600 hover:to-purple-700 hover:shadow-2xl hover:shadow-blue-500/25' 
                  : 'border-2 border-gray-700 text-gray-300 hover:border-gray-500 hover:bg-gray-800/50 hover:text-white'
              ]">
                <span class="relative z-10">Get Started</span>
                <div v-if="plan.popular" class="absolute inset-0 bg-gradient-to-r from-purple-600 to-blue-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- How to Deploy Section -->
    <section class="py-16 sm:py-20 lg:py-24 relative">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <div class="animate-fade-in-up">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
              Deploy in Minutes, Not Hours
            </h2>
            <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
              Get your SaaS application live with our streamlined deployment process.
            </p>
          </div>
        </div>
        
        <div class="max-w-4xl mx-auto">
          <div class="space-y-8">
            <div v-for="(step, index) in deploySteps" :key="step.title" 
                 class="flex flex-col md:flex-row items-start md:items-center gap-6 p-6 bg-gray-900/50 rounded-xl border border-gray-800/50 hover:border-gray-700/50 transition-all duration-500 transform hover:scale-105 backdrop-blur-sm group animate-fade-in-up"
                 :style="{ animationDelay: `${index * 0.2}s` }">
              <div class="flex-shrink-0">
                <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full flex items-center justify-center text-white font-bold text-lg transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12">
                  {{ index + 1 }}
                </div>
              </div>
              <div class="flex-grow">
                <h3 class="text-xl font-semibold text-white mb-2 group-hover:text-blue-400 transition-colors duration-300">{{ step.title }}</h3>
                <p class="text-gray-400 mb-4 group-hover:text-gray-300 transition-colors duration-300">{{ step.description }}</p>
                <div class="bg-gray-800/50 rounded-lg p-4 border border-gray-700/50 group-hover:border-gray-600/50 transition-colors duration-300">
                  <code class="text-sm text-green-400 font-mono">{{ step.command }}</code>
                </div>
              </div>
              <div class="flex-shrink-0">
                <span class="text-blue-400 text-2xl transition-transform duration-300 group-hover:scale-110">{{ step.icon }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="py-16 sm:py-20 lg:py-24 bg-gray-950/50 relative overflow-hidden">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <div class="animate-fade-in-up">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
              Loved by Developers Worldwide
            </h2>
            <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
              See what our community of developers and businesses are saying about SaaSify.
            </p>
          </div>
        </div>
        
        <div class="relative">
          <!-- Reviews Container -->
          <div class="overflow-hidden">
            <div class="flex transition-transform duration-500 ease-in-out" 
                 :style="{ transform: `translateX(-${currentReviewIndex * 100}%)` }">
              <div v-for="(review, index) in reviews" :key="index" 
                   class="w-full flex-shrink-0 px-4">
                <div class="max-w-4xl mx-auto">
                  <div class="bg-gray-900/50 rounded-2xl p-8 border border-gray-800/50 backdrop-blur-sm text-center group hover:border-gray-700/50 transition-all duration-500">
                    <div class="flex justify-center mb-6">
                      <div class="flex space-x-1">
                        <span v-for="star in 5" :key="star" class="text-yellow-400 text-xl">★</span>
                      </div>
                    </div>
                    <blockquote class="text-lg sm:text-xl text-gray-300 mb-8 leading-relaxed">
                      "{{ review.content }}"
                    </blockquote>
                    <div class="flex items-center justify-center space-x-4">
                      <PlaceholderImage :width="48" :height="48" class="rounded-full" />
                      <div class="text-left">
                        <div class="font-semibold text-white group-hover:text-blue-400 transition-colors duration-300">{{ review.name }}</div>
                        <div class="text-sm text-gray-400">{{ review.role }} at {{ review.company }}</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <!-- Navigation Buttons -->
          <button @click="previousReview" 
                  class="absolute left-4 top-1/2 transform -translate-y-1/2 bg-gray-900/80 hover:bg-gray-800 text-white p-3 rounded-full transition-all duration-300 hover:scale-110 backdrop-blur-sm border border-gray-700/50 hover:border-gray-600">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
            </svg>
          </button>
          <button @click="nextReview" 
                  class="absolute right-4 top-1/2 transform -translate-y-1/2 bg-gray-900/80 hover:bg-gray-800 text-white p-3 rounded-full transition-all duration-300 hover:scale-110 backdrop-blur-sm border border-gray-700/50 hover:border-gray-600">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
            </svg>
          </button>
          
          <!-- Dots Indicator -->
          <div class="flex justify-center mt-8 space-x-2">
            <button v-for="(review, index) in reviews" :key="index" 
                    @click="currentReviewIndex = index"
                    :class="[
                      'w-3 h-3 rounded-full transition-all duration-300',
                      currentReviewIndex === index 
                        ? 'bg-blue-500 scale-125' 
                        : 'bg-gray-600 hover:bg-gray-500'
                    ]">
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="py-16 sm:py-20 lg:py-24 relative">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <div class="animate-fade-in-up">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
              Frequently Asked Questions
            </h2>
            <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
              Everything you need to know about SaaSify. Can't find the answer you're looking for? 
              <a href="#contact" class="text-blue-400 hover:text-blue-300 transition-colors duration-300">Reach out to our team</a>.
            </p>
          </div>
        </div>
        
        <div class="space-y-4">
          <div v-for="(faq, index) in faqs" :key="index" 
               class="bg-gray-900/50 rounded-xl border border-gray-800/50 hover:border-gray-700/50 transition-all duration-300 backdrop-blur-sm animate-fade-in-up"
               :style="{ animationDelay: `${index * 0.1}s` }">
            <button @click="toggleFaq(index)" 
                    class="w-full px-6 py-6 text-left flex items-center justify-between hover:bg-gray-800/30 rounded-xl transition-all duration-300 group">
              <span class="text-lg font-semibold text-white group-hover:text-blue-400 transition-colors duration-300 pr-4">
                {{ faq.question }}
              </span>
              <svg :class="[
                     'w-5 h-5 text-gray-400 group-hover:text-blue-400 transition-all duration-300 flex-shrink-0',
                     openFaqIndex === index ? 'rotate-180' : ''
                   ]" 
                   fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
              </svg>
            </button>
            <transition
              enter-active-class="transition duration-300 ease-out"
              enter-from-class="transform scale-95 opacity-0"
              enter-to-class="transform scale-100 opacity-100"
              leave-active-class="transition duration-200 ease-in"
              leave-from-class="transform scale-100 opacity-100"
              leave-to-class="transform scale-95 opacity-0"
            >
              <div v-if="openFaqIndex === index" class="px-6 pb-6">
                <div class="text-gray-400 leading-relaxed border-t border-gray-800/50 pt-4">
                  {{ faq.answer }}
                </div>
              </div>
            </transition>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-16 sm:py-20 lg:py-24 bg-gradient-to-r from-blue-600 via-purple-600 to-blue-700 relative overflow-hidden">
      <div class="absolute inset-0 bg-black/20"></div>
      <div class="absolute inset-0 bg-gradient-to-r from-blue-600/50 to-purple-600/50 animate-gradient-x"></div>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
        <div class="animate-fade-in-up">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-6">
            Ready to Transform Your Business?
          </h2>
          <p class="text-lg sm:text-xl text-blue-100 max-w-3xl mx-auto mb-10">
            Join thousands of companies already using SaaSify to build amazing products and grow their business.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <button class="bg-white text-blue-600 px-8 py-4 rounded-lg text-lg font-semibold hover:bg-gray-100 transition-all duration-300 transform hover:scale-105 shadow-2xl hover:shadow-white/25 relative overflow-hidden group">
              <span class="relative z-10">Start Your Free Trial</span>
              <div class="absolute inset-0 bg-gradient-to-r from-gray-100 to-white opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </button>
            <button class="border-2 border-white text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-white hover:text-blue-600 transition-all duration-300 transform hover:scale-105 backdrop-blur-sm">
              Contact Sales
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer with Email Subscription -->
    <footer class="bg-gray-950 text-white py-12 sm:py-16 border-t border-gray-800/50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Newsletter Subscription Section -->
        <div class="mb-12 animate-fade-in-up">
          <div class="bg-gradient-to-r from-blue-500/10 to-purple-600/10 rounded-2xl p-8 border border-blue-500/20 backdrop-blur-sm">
            <div class="max-w-2xl mx-auto text-center">
              <h3 class="text-2xl sm:text-3xl font-bold text-white mb-4">
                Stay Updated with SaaSify
              </h3>
              <p class="text-gray-400 mb-6">
                Get the latest updates, feature releases, and developer tips delivered straight to your inbox.
              </p>
              <form @submit.prevent="subscribeEmail" class="flex flex-col sm:flex-row gap-4 max-w-md mx-auto">
                <div class="flex-grow relative">
                  <input 
                    v-model="emailInput"
                    type="email" 
                    placeholder="Enter your email address"
                    required
                    class="w-full px-4 py-3 bg-gray-900/50 border border-gray-700/50 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all duration-300 backdrop-blur-sm"
                  />
                  <div v-if="emailError" class="absolute -bottom-6 left-0 text-red-400 text-sm">
                    {{ emailError }}
                  </div>
                </div>
                <button 
                  type="submit"
                  :disabled="isSubscribing"
                  :class="[
                    'px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 relative overflow-hidden group',
                    isSubscribing 
                      ? 'bg-gray-600 cursor-not-allowed' 
                      : 'bg-gradient-to-r from-blue-500 to-purple-600 hover:from-blue-600 hover:to-purple-700 hover:shadow-lg hover:shadow-blue-500/25'
                  ]"
                >
                  <span class="relative z-10">
                    {{ isSubscribing ? 'Subscribing...' : 'Subscribe' }}
                  </span>
                  <div v-if="!isSubscribing" class="absolute inset-0 bg-gradient-to-r from-purple-600 to-blue-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </form>
              
              <!-- Success Message -->
              <transition
                enter-active-class="transition duration-300 ease-out"
                enter-from-class="transform scale-95 opacity-0"
                enter-to-class="transform scale-100 opacity-100"
                leave-active-class="transition duration-200 ease-in"
                leave-from-class="transform scale-100 opacity-100"
                leave-to-class="transform scale-95 opacity-0"
              >
                <div v-if="subscriptionSuccess" class="mt-4 p-4 bg-green-500/20 border border-green-500/30 rounded-lg">
                  <div class="flex items-center justify-center text-green-400">
                    <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                    <span>Thanks for subscribing! Check your email for confirmation.</span>
                  </div>
                </div>
              </transition>
              
              <p class="text-xs text-gray-500 mt-4">
                No spam, unsubscribe at any time. Read our 
                <a href="#privacy" class="text-blue-400 hover:text-blue-300 transition-colors duration-300">Privacy Policy</a>.
              </p>
            </div>
          </div>
        </div>

        <!-- Main Footer Content -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-8 mb-8">
          <!-- Company Info -->
          <div class="lg:col-span-2 animate-fade-in-up">
            <div class="flex items-center mb-4 group">
              <div class="w-8 h-8 bg-gradient-to-r from-blue-500 to-purple-600 rounded-lg flex items-center justify-center transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12">
                <span class="text-white font-bold text-sm">S</span>
              </div>
              <span class="ml-2 text-xl font-bold group-hover:text-blue-400 transition-colors duration-300">SaaSify</span>
            </div>
            <p class="text-gray-400 mb-6 max-w-md group-hover:text-gray-300 transition-colors duration-300">
              The complete platform for modern SaaS applications. Build faster, scale effortlessly, and focus on what matters most.
            </p>
            <div class="flex space-x-4">
              <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="Twitter">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
                </svg>
              </a>
              <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="LinkedIn">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </a>
              <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="GitHub">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
              </a>
              <a href="#" class="text-gray-400 hover:text-white transition-all duration-300 transform hover:scale-110 hover:-translate-y-1" aria-label="Discord">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.317 4.3698a19.7913 19.7913 0 00-4.8851-1.5152.0741.0741 0 00-.0785.0371c-.211.3753-.4447.8648-.6083 1.2495-1.8447-.2762-3.68-.2762-5.4868 0-.1636-.3933-.4058-.8742-.6177-1.2495a.077.077 0 00-.0785-.037 19.7363 19.7363 0 00-4.8852 1.515.0699.0699 0 00-.0321.0277C.5334 9.0458-.319 13.5799.0992 18.0578a.0824.0824 0 00.0312.0561c2.0528 1.5076 4.0413 2.4228 5.9929 3.0294a.0777.0777 0 00.0842-.0276c.4616-.6304.8731-1.2952 1.226-1.9942a.076.076 0 00-.0416-.1057c-.6528-.2476-1.2743-.5495-1.8722-.8923a.077.077 0 01-.0076-.1277c.1258-.0943.2517-.1923.3718-.2914a.0743.0743 0 01.0776-.0105c3.9278 1.7933 8.18 1.7933 12.0614 0a.0739.0739 0 01.0785.0095c.1202.099.246.1981.3728.2924a.077.077 0 01-.0066.1276 12.2986 12.2986 0 01-1.873.8914.0766.0766 0 00-.0407.1067c.3604.698.7719 1.3628 1.225 1.9932a.076.076 0 00.0842.0286c1.961-.6067 3.9495-1.5219 6.0023-3.0294a.077.077 0 00.0313-.0552c.5004-5.177-.8382-9.6739-3.5485-13.6604a.061.061 0 00-.0312-.0286zM8.02 15.3312c-1.1825 0-2.1569-1.0857-2.1569-2.419 0-1.3332.9555-2.4189 2.157-2.4189 1.2108 0 2.1757 1.0952 2.1568 2.419 0 1.3332-.9555 2.4189-2.1569 2.4189zm7.9748 0c-1.1825 0-2.1569-1.0857-2.1569-2.419 0-1.3332.9554-2.4189 2.1569-2.4189 1.2108 0 2.1757 1.0952 2.1568 2.419 0 1.3332-.9555 2.4189-2.1568 2.4189Z"/>
                </svg>
              </a>
            </div>
          </div>
          
          <!-- Product Links -->
          <div class="animate-fade-in-up" style="animation-delay: 0.1s;">
            <h4 class="text-lg font-semibold mb-4 text-white">Product</h4>
            <ul class="space-y-3">
              <li><a href="#features" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Features</a></li>
              <li><a href="#pricing" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Pricing</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">API Documentation</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Integrations</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Changelog</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Roadmap</a></li>
            </ul>
          </div>
          
          <!-- Company Links -->
          <div class="animate-fade-in-up" style="animation-delay: 0.2s;">
            <h4 class="text-lg font-semibold mb-4 text-white">Company</h4>
            <ul class="space-y-3">
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">About Us</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Blog</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Careers</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Press Kit</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Partners</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Contact</a></li>
            </ul>
          </div>
          
          <!-- Support & Legal Links -->
          <div class="animate-fade-in-up" style="animation-delay: 0.3s;">
            <h4 class="text-lg font-semibold mb-4 text-white">Support & Legal</h4>
            <ul class="space-y-3">
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Help Center</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Community</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Status Page</a></li>
              <li><a href="#privacy" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Privacy Policy</a></li>
              <li><a href="#terms" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Terms of Service</a></li>
              <li><a href="#cookies" class="text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">Cookie Policy</a></li>
            </ul>
          </div>
        </div>
        
        <!-- Bottom Footer -->
        <div class="border-t border-gray-800 pt-8">
          <div class="flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0 animate-fade-in-up" style="animation-delay: 0.4s;">
          <!-- Copyright -->
            <div class="text-gray-400 text-sm">
              © 2024 SaaSify. All rights reserved.
            </div>
            
            <!-- Legal Links -->
            <div class="flex flex-wrap justify-center md:justify-end space-x-6 text-sm">
              <a href="#privacy" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
              <a href="#terms" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
              <a href="#cookies" class="text-gray-400 hover:text-white transition-colors duration-300">Cookies</a>
              <a href="#security" class="text-gray-400 hover:text-white transition-colors duration-300">Security</a>
              <a href="#accessibility" class="text-gray-400 hover:text-white transition-colors duration-300">Accessibility</a>
            </div>
            
            <!-- Language/Region Selector -->
            <div class="flex items-center space-x-2 text-sm">
              <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
              </svg>
              <select class="bg-transparent text-gray-400 hover:text-white transition-colors duration-300 focus:outline-none cursor-pointer">
                <option value="en">English (US)</option>
                <option value="es">Español</option>
                <option value="fr">Français</option>
                <option value="de">Deutsch</option>
                <option value="ja">日本語</option>
              </select>
            </div>
          </div>
          
          <!-- Trust Badges -->
          <div class="mt-8 pt-6 border-t border-gray-800/50">
            <div class="flex flex-wrap justify-center items-center space-x-8 space-y-4 md:space-y-0 animate-fade-in-up" style="animation-delay: 0.5s;">
              <div class="flex items-center space-x-2 text-gray-400 text-sm">
                <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
                </svg>
                <span>SOC 2 Compliant</span>
              </div>
              <div class="flex items-center space-x-2 text-gray-400 text-sm">
                <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
                </svg>
                <span>GDPR Ready</span>
              </div>
              <div class="flex items-center space-x-2 text-gray-400 text-sm">
                <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                </svg>
                <span>99.9% Uptime</span>
              </div>
              <div class="flex items-center space-x-2 text-gray-400 text-sm">
                <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                </svg>
                <span>Global CDN</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import PlaceholderImage from './components/PlaceholderImage.vue'

const mobileMenuOpen = ref(false)
const currentReviewIndex = ref(0)
const openFaqIndex = ref(null)
const emailInput = ref('')
const isSubscribing = ref(false)
const subscriptionSuccess = ref(false)
const emailError = ref('')

// Email subscription method
const subscribeEmail = async () => {
  if (!emailInput.value) {
    emailError.value = 'Please enter your email address'
    return
  }
  
  if (!isValidEmail(emailInput.value)) {
    emailError.value = 'Please enter a valid email address'
    return
  }
  
  emailError.value = ''
  isSubscribing.value = true
  
  try {
    // Simulate API call
    await new Promise(resolve => setTimeout(resolve, 1500))
    
    subscriptionSuccess.value = true
    emailInput.value = ''
    
    // Hide success message after 5 seconds
    setTimeout(() => {
      subscriptionSuccess.value = false
    }, 5000)
    
  } catch (error) {
    emailError.value = 'Something went wrong. Please try again.'
  } finally {
    isSubscribing.value = false
  }
}

// Email validation helper
const isValidEmail = (email) => {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
  return emailRegex.test(email)
}

// Auto-rotate reviews
let reviewInterval

// Review navigation methods
const nextReview = () => {
  currentReviewIndex.value = (currentReviewIndex.value + 1) % reviews.length
}

const previousReview = () => {
  currentReviewIndex.value = currentReviewIndex.value === 0 ? reviews.length - 1 : currentReviewIndex.value - 1
}

// FAQ toggle method
const toggleFaq = (index) => {
  openFaqIndex.value = openFaqIndex.value === index ? null : index
}

onMounted(() => {
  // Start auto-rotation for reviews
  reviewInterval = setInterval(() => {
    nextReview()
  }, 5000)
})

onUnmounted(() => {
  if (reviewInterval) {
    clearInterval(reviewInterval)
  }
})

// Features data
const features = [
  {
    title: 'Lightning Fast',
    description: 'Built for speed with modern technologies and optimized performance that scales.',
    icon: '⚡'
  },
  {
    title: 'Secure by Default',
    description: 'Enterprise-grade security with end-to-end encryption and compliance standards.',
    icon: '🔒'
  },
  {
    title: 'Scalable Infrastructure',
    description: 'Auto-scaling infrastructure that grows seamlessly with your business needs.',
    icon: '📈'
  },
  {
    title: 'Real-time Analytics',
    description: 'Comprehensive analytics and insights to drive data-driven business decisions.',
    icon: '📊'
  },
  {
    title: 'API First',
    description: 'Powerful APIs and webhooks for seamless integrations with your existing tools.',
    icon: '🔌'
  },
  {
    title: '24/7 Support',
    description: 'Round-the-clock support from our expert team whenever you need assistance.',
    icon: '🎧'
  }
]

// Stats data
const stats = [
  { value: '10K+', label: 'Active Users' },
  { value: '99.9%', label: 'Uptime' },
  { value: '50+', label: 'Integrations' },
  { value: '24/7', label: 'Support' }
]

// Pricing plans
const pricingPlans = [
  {
    name: 'Starter',
    price: 29,
    popular: false,
    features: [
      'Up to 1,000 users',
      'Basic analytics',
      'Email support',
      'API access',
      '5GB storage'
    ]
  },
  {
    name: 'Professional',
    price: 99,
    popular: true,
    features: [
      'Up to 10,000 users',
      'Advanced analytics',
      'Priority support',
      'Full API access',
      '100GB storage',
      'Custom integrations'
    ]
  },
  {
    name: 'Enterprise',
    price: 299,
    popular: false,
    features: [
      'Unlimited users',
      'Custom analytics',
      'Dedicated support',
      'White-label solution',
      'Unlimited storage',
      'Custom development'
    ]
  }
]

// Deploy steps data
const deploySteps = [
  {
    title: 'Connect Your Repository',
    description: 'Link your GitHub, GitLab, or Bitbucket repository to SaaSify with one click.',
    command: 'git clone https://github.com/your-repo/saas-app.git',
    icon: '🔗'
  },
  {
    title: 'Configure Environment',
    description: 'Set up your environment variables and database connections through our intuitive dashboard.',
    command: 'saasify env:setup --auto-detect',
    icon: '⚙️'
  },
  {
    title: 'Deploy Instantly',
    description: 'Hit deploy and watch your application go live with automatic SSL, CDN, and scaling.',
    command: 'saasify deploy --production',
    icon: '🚀'
  },
  {
    title: 'Monitor & Scale',
    description: 'Track performance, monitor errors, and scale automatically based on traffic demands.',
    command: 'saasify monitor --real-time',
    icon: '📈'
  }
]

// Reviews data
const reviews = [
  {
    content: "SaaSify transformed our development workflow. We went from months of setup to deploying in minutes. The auto-scaling feature alone saved us thousands in infrastructure costs.",
    name: "Sarah Chen",
    role: "CTO",
    company: "TechFlow",
    avatar: "avatar-1"
  },
  {
    content: "The developer experience is incredible. The API-first approach and real-time analytics gave us insights we never had before. Our team productivity increased by 300%.",
    name: "Marcus Rodriguez",
    role: "Lead Developer",
    company: "InnovateLabs",
    avatar: "avatar-2"
  },
  {
    content: "Security was our biggest concern when choosing a platform. SaaSify's enterprise-grade security and compliance features gave us the confidence to migrate our entire infrastructure.",
    name: "Emily Watson",
    role: "Security Engineer",
    company: "SecureBase",
    avatar: "avatar-3"
  },
  {
    content: "The 24/7 support team is phenomenal. They helped us optimize our deployment pipeline and reduced our build times by 70%. Couldn't be happier with the service.",
    name: "David Kim",
    role: "DevOps Manager",
    company: "CloudNative",
    avatar: "avatar-4"
  },
  {
    content: "From startup to enterprise scale, SaaSify grew with us. The pricing is transparent, the features are robust, and the performance is unmatched. Highly recommended!",
    name: "Lisa Thompson",
    role: "Founder",
    company: "StartupSuccess",
    avatar: "avatar-5"
  }
]

// FAQ data
const faqs = [
  {
    question: "How quickly can I deploy my application?",
    answer: "Most applications can be deployed within 2-3 minutes after connecting your repository. Our automated deployment pipeline handles everything from dependency installation to SSL certificate provisioning."
  },
  {
    question: "What frameworks and languages do you support?",
    answer: "We support all major frameworks including React, Vue, Angular, Next.js, Nuxt, Express, Django, Rails, and many more. Our platform automatically detects your framework and optimizes the deployment accordingly."
  },
  {
    question: "How does the pricing work?",
    answer: "Our pricing is based on usage and features. The Starter plan includes everything you need to get started, while Professional and Enterprise plans offer advanced features like custom integrations and dedicated support. No hidden fees, ever."
  },
  {
    question: "Is my data secure?",
    answer: "Absolutely. We use enterprise-grade security with end-to-end encryption, SOC 2 compliance, and regular security audits. Your data is stored in secure, geographically distributed data centers with automatic backups."
  },
  {
    question: "Can I migrate from my current hosting provider?",
    answer: "Yes! Our migration team provides free assistance to help you move from any hosting provider. We support database migrations, DNS transfers, and can help minimize downtime during the transition."
  },
  {
    question: "Do you offer custom integrations?",
    answer: "Professional and Enterprise plans include custom integrations. Our API-first approach makes it easy to connect with your existing tools, and our team can help build custom solutions for your specific needs."
  },
  {
    question: "What kind of support do you provide?",
    answer: "We offer 24/7 email support for all plans, with priority support and dedicated account managers for Professional and Enterprise customers. Our average response time is under 2 hours."
  },
  {
    question: "Can I scale my application automatically?",
    answer: "Yes, auto-scaling is included in all plans. Your application automatically scales up during traffic spikes and scales down during quiet periods, ensuring optimal performance while controlling costs."
  }
]
</script>

<style scoped>
/* Dark theme with Vercel-inspired design */
.bg-clip-text {
  -webkit-background-clip: text;
  background-clip: text;
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Enhanced gradient animations */
@keyframes gradient-x {
  0%, 100% {
    transform: translateX(0%);
  }
  50% {
    transform: translateX(100%);
  }
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.animate-gradient-x {
  background-size: 200% 200%;
  animation: gradient 3s ease infinite;
}

/* Fade in up animation */
@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
  opacity: 0;
}

/* Pulse animation for background elements */
@keyframes pulse {
  0%, 100% {
    opacity: 0.3;
    transform: scale(1);
  }
  50% {
    opacity: 0.5;
    transform: scale(1.05);
  }
}

/* Custom scrollbar for dark theme */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #1f2937;
}

::-webkit-scrollbar-thumb {
  background: #4b5563;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #6b7280;
}

/* Backdrop blur support */
.backdrop-blur-xl {
  backdrop-filter: blur(24px);
}

.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Mobile optimizations */
@media (max-width: 768px) {
  .animate-fade-in-up {
    animation-duration: 0.6s;
  }
}

/* Reduced motion for accessibility */
@media (prefers-reduced-motion: reduce) {
  .animate-fade-in-up,
  .animate-gradient-x,
  .animate-pulse {
    animation: none;
  }
  
  * {
    transition-duration: 0.01ms !important;
  }
}
</style>