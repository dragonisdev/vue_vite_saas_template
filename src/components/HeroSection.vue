<template>
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
</template>

<script setup>
import PlaceholderImage from './PlaceholderImage.vue'
</script> 