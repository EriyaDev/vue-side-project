<script setup>
import AllComponents from '@/components/Home/AllComponents.vue'
import AllSections from '@/components/Home/AllSections.vue'
import HeroSection from '@/components/Home/HeroSection.vue'

import { ref, onMounted } from 'vue'

const isVisible = ref(false)

onMounted(() => {
  requestAnimationFrame(() => {
    isVisible.value = true
  })
})
</script>

<template>
  <div
    class="transition-all"
    :class="isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
  >
    <HeroSection />
    <AllComponents />
    <AllSections />
  </div>
</template>
