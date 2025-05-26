<template>
  <section class="py-16 sm:py-20 lg:py-24 bg-gray-950 text-white relative">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="mb-12 animate-fade-in-up">
        <div class="bg-gradient-to-r from-blue-500/10 to-purple-600/10 rounded-2xl p-8 border border-blue-500/20 backdrop-blur-sm">
          <div class="max-w-2xl mx-auto text-center">
            <h3 class="text-2xl sm:text-3xl font-bold text-white mb-4">
              Stay Updated with SaaSify
            </h3>
            <p class="text-gray-400 mb-6">
              Get the latest updates, feature releases, and developer tips delivered straight to your inbox.
            </p>
            <form @submit.prevent="handleSubmit" class="flex flex-col sm:flex-row gap-4 max-w-md mx-auto">
              <div class="flex-grow relative">
                <input 
                  v-model="email"
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
                  'px-6 py-3 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 relative overflow-hidden group whitespace-nowrap',
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
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const emailError = ref('')
const isSubscribing = ref(false)
const subscriptionSuccess = ref(false)

const handleSubmit = async () => {
  emailError.value = ''
  isSubscribing.value = true
  
  try {
    // Simulate API call
    await new Promise(resolve => setTimeout(resolve, 1000))
    subscriptionSuccess.value = true
    email.value = ''
  } catch (error) {
    emailError.value = 'Something went wrong. Please try again.'
  } finally {
    isSubscribing.value = false
  }
}
</script> 