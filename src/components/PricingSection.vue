<template>
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
</template>

<script setup>
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
</script> 