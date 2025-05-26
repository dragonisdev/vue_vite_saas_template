<template>
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
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import PlaceholderImage from './PlaceholderImage.vue'

const currentReviewIndex = ref(0)

// Review navigation methods
const nextReview = () => {
  currentReviewIndex.value = (currentReviewIndex.value + 1) % reviews.length
}

const previousReview = () => {
  currentReviewIndex.value = currentReviewIndex.value === 0 ? reviews.length - 1 : currentReviewIndex.value - 1
}

// Auto-rotate reviews
let reviewInterval

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
</script> 