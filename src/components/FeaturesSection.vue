<template>
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
</template>

<script setup>
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
    icon: '��'
  }
]
</script> 