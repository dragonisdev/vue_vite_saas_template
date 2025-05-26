<template>
  <div 
    class="bg-gradient-to-r from-blue-500/20 to-purple-600/20 rounded-lg flex items-center justify-center"
    :style="{ width: width + 'px', height: height + 'px' }"
  >
    <span class="text-gray-400 text-sm">Image Placeholder</span>
  </div>
</template>

<script setup>
defineProps({
  width: {
    type: [Number, String],
    default: 800
  },
  height: {
    type: [Number, String],
    default: 400
  }
})
</script> 