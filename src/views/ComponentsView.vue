<script setup>
import ComponentObject from '@/components/ComponentObject.vue'
</script>

<template>
  <div class="min-h-screen grid grid-cols-1 lg:grid-cols-[250px_1fr]">
    <!-- Sidebar -->
    <aside class="hidden lg:block bg-gray-50 border-r border-gray-200 p-4 h-full">
      <nav class="space-y-2 mt-20">
        <!-- Navigation items -->
        <h2 class="text-body font-semibold">COMPONENTS</h2>
        <div class="flex flex-col gap-1.5 mt-4">
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#button"
            >Buttons</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#card"
            >Cards</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#input"
            >Inputs</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#textarea"
            >Text Areas</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#pagination"
            >Pagination</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#badge"
            >Badges</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#select"
            >Select Options</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#breadcrumbs"
            >Breadcrumbs</router-link
          >
        </div>
      </nav>
    </aside>

    <!-- Main content area -->
    <main class="p-6 overflow-auto mt-20">
      <!-- Dashboard content -->
      <div class="flex flex-col gap-6">
        <div class="flex flex-col gap-2">
          <h1 class="medium-heading font-medium">Buttons</h1>
          <p class="text-body opacity-55 lg:max-w-[60%]">
            Reusable, accessible buttons with multiple variants, sizes, and states. Fully responsive
            and easily customizable using TailwindCSS utility classes for production-ready
            interfaces.
          </p>
        </div>

        <component-object
          :name="'Button'"
          :code="`
          <button 
            class='bg-button-primary text-white font-space-mono text-base  py-3 px-6 rounded-full hover:bg-avocado-1000/75 transition-colors duration-300 hover:cursor-pointer uppercase'>
            Button
          </button>
          `"
        ></component-object>
      </div>
    </main>
  </div>
</template>
