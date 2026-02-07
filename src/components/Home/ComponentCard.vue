<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  content: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div
    class="w-full h-64 bg-secondary border border-text-secondary/30 rounded-lg flex flex-col justify-start items-center hover:border-avocado-500 group transition-all duration-300"
  >
    <div
      class="w-full h-10 border-b border-text-secondary/30 group-hover:border-avocado-500 transition-all duration-300 rounded-t-md mb-3 py-1 px-3"
    >
      <h4 class="small-heading font-semibold leading-none">{{ props.title }}</h4>
    </div>
    <div class="w-full h-full flex justify-center items-center">
      <div v-html="props.content"></div>
    </div>
  </div>
</template>
