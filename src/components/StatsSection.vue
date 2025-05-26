<template>
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
</template>

<script setup>
const stats = [
  { value: '10K+', label: 'Active Users' },
  { value: '99.9%', label: 'Uptime' },
  { value: '50+', label: 'Integrations' },
  { value: '24/7', label: 'Support' }
]
</script> 