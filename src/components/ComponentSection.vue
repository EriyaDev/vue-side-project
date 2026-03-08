<script setup>
const props = defineProps({
  id: {
    type: String,
    required: true,
  },
  name: {
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
  <div :id="props.id" class="flex flex-col gap-6 mb-20">
    <div class="flex flex-col gap-2">
      <h1 class="medium-heading font-medium">{{ props.name }}</h1>
      <p class="text-body opacity-55 lg:max-w-[60%]">
        {{ props.description }}
      </p>
    </div>

    <slot></slot>
  </div>
</template>
