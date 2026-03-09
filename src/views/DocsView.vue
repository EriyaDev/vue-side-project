<script setup>
import ComponentObject from '@/components/ComponentObject.vue'
import ComponentSection from '@/components/ComponentSection.vue'
import OnlyCode from '@/components/OnlyCode.vue'

import { ref, onMounted } from 'vue'

const isVisible = ref(false)

onMounted(() => {
  requestAnimationFrame(() => {
    isVisible.value = true
  })
})
</script>

<template>
  <div class="min-h-screen grid grid-cols-1 lg:grid-cols-[250px_1fr]">
    <!-- Sidebar -->
    <aside class="hidden lg:block bg-gray-50 border-r border-gray-200 p-4 h-full">
      <nav class="space-y-2 mt-20 fixed">
        <!-- Navigation items -->
        <h2 class="text-body font-semibold">DOCS</h2>
        <div class="flex flex-col gap-1.5 mt-4">
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/docs#introduction"
            >Introduction</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/docs#quick-start"
            >Quick Start</router-link
          >
        </div>
      </nav>
    </aside>

    <!-- Main content area -->
    <main class="p-6 overflow-auto">
      <!-- Dashboard content -->
      <div
        class="grid grid-cols-1 gap-6 mt-20 transition-all"
        :class="isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
      >
        <div class="flex flex-col gap-6 mb-20">
          <div class="flex flex-col gap-2">
            <h1 class="medium-heading font-medium">Introduction</h1>
            <p class="text-body opacity-55 lg:max-w-[60%]">
              Welcome to <span class="font-semibold">Nexa UI</span>, a comprehensive collection of
              modern, accessible, and fully customizable UI components built with
              <span class="font-semibold">Tailwind CSS.</span>
              <br />
              <br />
              Nexa UI is designed to help developers build high-quality web interfaces faster.
              Instead of spending hours styling basic elements or wrestling with complex frameworks,
              you can leverage our pre-built components to focus on what truly matters:<span
                class="font-semibold"
              >
                building your application's logic and user experience.</span
              >
            </p>
          </div>
        </div>
      </div>

      <component-section
        id="quick-start"
        name="Quick Start"
        description="Get up and running with Nexa UI in seconds. Since our components are built entirely with Tailwind CSS utility classes, the setup is straightforward."
      >
        <div class="flex flex-col gap-10">
          <div class="flex flex-col gap-1">
            <h2 class="text-body font-semibold">Install Tailwind CSS</h2>
            <p class="text-body opacity-55 lg:max-w-[60%]">
              Ensure you have Tailwind CSS installed and configured in your project. If you haven't,
              follow the
              <a class="link" href="https://tailwindcss.com/docs/installation/"
                >official installation guide.</a
              >
            </p>
          </div>

          <div class="flex flex-col gap-1">
            <h2 class="text-body font-semibold">Install Remix Icon</h2>
            <p class="text-body opacity-55 lg:max-w-[60%] mb-2">
              Nexa UI uses <a class="link" href="https://remixicon.com/">Remix Icon</a> for clean,
              consistent iconography.
            </p>

            <OnlyCode name="Install Remix Icon" code="npm install remixicon --save"></OnlyCode>

            <p class="text-small">
              and add

              <code
                class="bg-avocado-200 w-fit text-avocado-900 text-sm px-2 py-0.5 rounded-full border border-avocado-400"
                >@import 'remixicon/fonts/remixicon.css';</code
              >
              in your CSS file
            </p>
          </div>

          <div class="flex flex-col gap-1">
            <h2 class="text-body font-semibold">Optimized Configuration</h2>
            <p class="text-body opacity-55 lg:max-w-[60%]">
              To achieve the best visual results and ensure full compatibility with Nexa UI
              components, update your CSS file with the following configuration:
            </p>

            <OnlyCode
              name="Configuration"
              :code="`
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:ital,wght@0,100..900;1,100..900&family=Manrope:wght@200..800&family=Space+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap');
/* @import 'remixicon/fonts/remixicon.css'; goes here*/
/* @import 'tailwindcss'; goes here*/

/* Custom Variable */
@theme {
  --font-manrope: 'Manrope', 'sans-serif';
  --font-grotesk: 'Hanken Grotesk', 'sans-serif';
  --font-space-mono: 'Space Mono', 'monospace';
  --breakpoint-3xl: 120rem;

  --color-primary: #fafafa;
  --color-primary: #ffffff;

  --color-button-primary: #1d1d1d;
  --color-button-secondary: #ffffff;

  --color-text-primary: #1c1c1c;
  --color-text-secondary: #525252;

  --color-avocado-100: oklch(0.99 0 0);
  --color-avocado-200: oklch(0.98 0.04 113.22);
  --color-avocado-300: oklch(0.94 0.11 115.03);
  --color-avocado-400: oklch(0.92 0.19 114.08);
  --color-avocado-450: oklch(0.88 0.18 117.33);
  --color-avocado-500: oklch(0.84 0.18 117.33);
  --color-avocado-600: oklch(0.53 0.12 118.34);
  --color-avocado-700: oklch(0.45 0.12 118.34);
  --color-avocado-800: oklch(0.38 0.12 118.34);
  --color-avocado-900: oklch(0.3 0.12 118.34);
  --color-avocado-1000: oklch(0.2 0.12 118.34);
}
          `"
            ></OnlyCode>
          </div>

          <div class="flex flex-col gap-1">
            <h2 class="text-body font-semibold">Copy & Paste</h2>
            <p class="text-body opacity-55 lg:max-w-[60%]">
              You are all set! Browse our library, find the component you need, and simply copy the
              code directly into your project files.
            </p>

            <router-link to="/components" class="btn-primary group mt-2 w-fit"
              >See All Components
              <i class="ri-arrow-right-line text-white group-hover:ml-2 transition-all"></i
            ></router-link>
          </div>
        </div>
      </component-section>
    </main>
  </div>
</template>
