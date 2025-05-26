<template>
  <div class="min-h-screen bg-gray-950">
    <TheHeader />
    <main>
      <HeroSection />
      <FeaturesSection />
      <StatsSection />
      <PricingSection />
      <DeploySection />
      <ReviewsSection />
      <FaqSection />
      <CtaBanner />
      <SubscribeSection />
    </main>
    <TheFooter />
  </div>
</template>

<script setup>
import TheHeader from './components/TheHeader.vue'
import HeroSection from './components/HeroSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import StatsSection from './components/StatsSection.vue'
import PricingSection from './components/PricingSection.vue'
import DeploySection from './components/DeploySection.vue'
import ReviewsSection from './components/ReviewsSection.vue'
import FaqSection from './components/FaqSection.vue'
import CtaBanner from './components/CtaBanner.vue'
import SubscribeSection from './components/SubscribeSection.vue'
import TheFooter from './components/TheFooter.vue'
</script>