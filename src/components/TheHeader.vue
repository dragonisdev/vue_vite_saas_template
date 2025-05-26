<template>
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
            <a v-for="item in navigationItems" :key="item.href" 
               :href="item.href" 
               class="text-gray-400 hover:text-white px-3 py-2 text-sm font-medium transition-all duration-300 hover:scale-105 relative group">
              {{ item.text }}
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
          <a v-for="item in navigationItems" :key="item.href"
             :href="item.href" 
             class="block px-3 py-2 text-base font-medium text-gray-400 hover:text-white transition-all duration-300 hover:translate-x-2">
            {{ item.text }}
          </a>
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
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const navigationItems = [
  { text: 'Features', href: '#features' },
  { text: 'Pricing', href: '#pricing' },
  { text: 'Reviews', href: '#reviews' },
  { text: 'FAQ', href: '#faq' }
]
</script> 