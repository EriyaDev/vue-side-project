<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import { useDarkMode } from '@/composables/useDarkMode'

// const { isDark, toggleDark } = useDarkMode()
</script>

<template>
  <div
    class="header bg-primary w-full py-4 fixed top-0 left-0 z-50 border-b border-b-text-secondary/10"
  >
    <nav class="container mx-auto flex flex-row items-center justify-between">
      <RouterLink to="/" class="text-xl font-bold font-grotesk"
        ><span class="text-avocado-600">Nexa</span> UI</RouterLink
      >

      <ul class="flex flex-row items-center space-x-4">
        <li><RouterLink class="navbar-link" to="/">Home</RouterLink></li>
        <li><RouterLink class="navbar-link" to="/components">Components</RouterLink></li>
        <li><RouterLink class="navbar-link" to="/docs">Documentation</RouterLink></li>
        <li>
          <a class="navbar-link" href="https://github.com/EriyaDev/vue-side-project"
            ><i class="ri-github-fill text-xl"></i
          ></a>
        </li>
        <!-- <li>
          <button
            id="dark-mode-toggle"
            @click="toggleDark"
            :aria-label="isDark ? 'Switch to light mode' : 'Switch to dark mode'"
            class="theme-toggle-btn"
          >
            <span class="theme-toggle-icon" :class="{ 'is-dark': isDark }">
              <i class="ri-sun-line sun-icon"></i>
              <i class="ri-moon-line moon-icon"></i>
            </span>
          </button>
        </li> -->
      </ul>
    </nav>
  </div>
  <RouterView v-slot="{ Component }">
    <Transition name="page" mode="out-in">
      <component :is="Component" />
    </Transition>
  </RouterView>
</template>

<style>
.page-enter-active,
.page-leave-active {
  transition:
    opacity 0.3s ease,
    transform 0.3s ease;
}
.page-enter-from {
  opacity: 0;
  transform: translateY(12px);
}
.page-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}
</style>
