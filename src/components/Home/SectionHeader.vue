<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="container mx-auto section-header">
    <h1 class="medium-heading font-semibold line-clamp-2">{{ props.title }}</h1>
    <p class="text-body max-w-[50%] text-center line-clamp-2">
      {{ props.description }}
    </p>
  </div>
</template>
