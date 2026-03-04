<script setup>
import { ref, computed } from 'vue'
import hljs from 'highlight.js/lib/core'
import xml from 'highlight.js/lib/languages/xml'

hljs.registerLanguage('xml', xml)

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  code: {
    type: String,
    required: true,
  },
})

const activeTab = ref('component')
const copied = ref(false)

function copyCode() {
  navigator.clipboard.writeText(props.code).then(() => {
    copied.value = true
    setTimeout(() => (copied.value = false), 2000)
  })
}

const highlightCode = computed(() =>
  hljs.highlight(props.code, { language: 'xml' }).value
)
</script>

<template>
  <div class="w-full lg:max-w-[60%] border border-text-primary/10 rounded-2xl">
    <div
      class="w-full border-b border-b-text-primary/10 p-4 justify-between items-center flex gap-4"
    >
      <p class="text-body font-medium">{{ props.name }}</p>

      <div class="flex gap-2">
        <button
          class="flex items-center gap-2 border border-text-primary/10 rounded-lg py-0.5 px-2"
          :class="{ 'bg-text-primary/10': activeTab === 'code' }"
          @click="activeTab = activeTab === 'code' ? 'component' : 'code'"
        >
          <i class="ri-code-s-slash-line"></i>
          <p class="text-small text-text-primary/70">Code</p>
        </button>
        <button
          class="flex items-center gap-2 border border-text-primary/10 rounded-lg py-0.5 px-2 transition-colors duration-200"
          :class="{ 'bg-text-primary/10': copied }"
          @click="copyCode"
        >
          <i :class="copied ? 'ri-check-line' : 'ri-file-copy-line'"></i>
          <p class="text-small text-text-primary/70">{{ copied ? 'Copied!' : 'Copy' }}</p>
        </button>
      </div>
    </div>
    <div class="min-h-20 p-4 flex justify-center items-center">
      <!-- COMPONENT TAB -->
      <div v-show="activeTab === 'component'" v-html="props.code"></div>

      <!-- CODE TAB -->
      <pre
        v-show="activeTab === 'code'"
        class="w-full text-small overflow-x-auto whitespace-pre-wrap hljs"
      ><code v-html="highlightCode"></code></pre>
    </div>
  </div>
</template>
