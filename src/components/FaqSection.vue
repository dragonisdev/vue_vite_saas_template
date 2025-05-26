<template>
  <section id="faq" class="py-16 sm:py-20 lg:py-24 bg-gray-950/50 relative">
    <div class="absolute inset-0 bg-gradient-to-b from-transparent via-gray-950/20 to-transparent"></div>
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="text-center mb-16">
        <div class="animate-fade-in-up">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Frequently Asked Questions
          </h2>
          <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto">
            Everything you need to know about our platform and services.
          </p>
        </div>
      </div>
      
      <div class="max-w-3xl mx-auto space-y-4">
        <div v-for="(faq, index) in faqs" :key="faq.question" 
             class="bg-gray-900/50 rounded-xl overflow-hidden border border-gray-800/50 hover:border-gray-700/50 transition-all duration-300 animate-fade-in-up"
             :style="{ animationDelay: `${index * 0.1}s` }">
          <button @click="toggleFaq(index)" 
                  class="w-full px-6 py-4 text-left flex items-center justify-between focus:outline-none group">
            <span class="text-lg font-medium text-white group-hover:text-blue-400 transition-colors duration-300">
              {{ faq.question }}
            </span>
            <span class="text-gray-400 group-hover:text-blue-400 transition-colors duration-300">
              {{ openFaqIndex === index ? '−' : '+' }}
            </span>
          </button>
          <div v-show="openFaqIndex === index" 
               class="px-6 pb-4 text-gray-400 animate-fade-in">
            {{ faq.answer }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const openFaqIndex = ref(null)

const toggleFaq = (index) => {
  openFaqIndex.value = openFaqIndex.value === index ? null : index
}

const faqs = [
  {
    question: 'What makes this template different from others?',
    answer: 'Our template is built with modern technologies and best practices, featuring a beautiful design, responsive layout, and optimized performance. It includes all the essential components for a SaaS application, with a focus on user experience and developer productivity.'
  },
  {
    question: 'Do I need to be a developer to use this template?',
    answer: 'While some technical knowledge is helpful, we\'ve designed the template to be as user-friendly as possible. The documentation includes detailed instructions for customization, and our support team is always available to help you get started.'
  },
  {
    question: 'Can I customize the design and features?',
    answer: 'Absolutely! The template is built with flexibility in mind. You can easily customize colors, typography, layouts, and add or remove features to match your specific needs. All components are modular and well-documented.'
  },
  {
    question: 'What kind of support do you offer?',
    answer: 'We offer comprehensive support through documentation, email support, and a community forum. Our team is dedicated to helping you succeed with your project, whether you need technical assistance or guidance on best practices.'
  },
  {
    question: 'Is the template mobile-friendly?',
    answer: 'Yes! The template is fully responsive and works beautifully on all devices, from mobile phones to desktop computers. We\'ve implemented mobile-first design principles to ensure the best experience across all screen sizes.'
  }
]
</script> 