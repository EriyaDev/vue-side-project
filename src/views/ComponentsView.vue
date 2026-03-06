<script setup>
import ComponentObject from '@/components/ComponentObject.vue'
import ComponentSection from '@/components/ComponentSection.vue'
</script>

<template>
  <div class="min-h-screen grid grid-cols-1 lg:grid-cols-[250px_1fr]">
    <!-- Sidebar -->
    <aside class="hidden lg:block bg-gray-50 border-r border-gray-200 p-4 h-full">
      <nav class="space-y-2 mt-20 fixed">
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

      <component-section
        name="Buttons"
        description="Reusable, accessible buttons with multiple variants, sizes, and states. Fully responsive
            and easily customizable using TailwindCSS utility classes for production-ready
            interfaces."
      >
        <component-object
          :name="'Button'"
          :code="`
          <button 
            class='bg-black text-white font-space-mono text-base  py-3 px-6 rounded-full hover:bg-black/75 transition-colors duration-300 hover:cursor-pointer uppercase'>
            Button
          </button>

          <button 
            class='bg-white text-black font-space-mono text-base  py-3 px-6 rounded-full border border-black/20 hover:bg-black/5 transition-all hover:cursor-pointer uppercase'>
            Button
          </button>
          `"
        ></component-object>

        <component-object
          :name="'Button Invert Color on Hover'"
          :code="`
          <button 
            class='bg-black text-white font-space-mono text-base border py-3 px-6 rounded-full hover:bg-white hover:text-black  transition-all hover: duration-300 hover:cursor-pointer uppercase'>
            Button
          </button>

          <button 
            class='bg-white text-black font-space-mono text-base border py-3 px-6 rounded-full hover:bg-black hover:text-white  transition-all hover: duration-300 hover:cursor-pointer uppercase'>
            Button
          </button>
          `"
        ></component-object>

        <component-object
          :name="'Button with Icon'"
          :code="`
          <button 
            class='bg-black text-white font-space-mono text-base  py-3 px-6 rounded-full hover:bg-black/75 transition-colors duration-300 hover:cursor-pointer uppercase'>
            <i class='ri-add-circle-fill text-white'></i>
            Button
          </button>

          <button 
            class='bg-white text-black font-space-mono text-base  py-3 px-6 rounded-full border border-black/20 hover:bg-black/5 transition-all hover:cursor-pointer uppercase'>
            <i class='ri-add-circle-fill text-black'></i>
            Button
          </button>
          `"
        ></component-object>

        <component-object
          :name="'Button with Icon Animation'"
          :code="`
          <button 
            class='bg-black text-white font-space-mono text-base py-3 px-6 rounded-full hover:bg-black/75 transition-colors duration-300 hover:cursor-pointer uppercase group'>
            Button
            <i class='ri-arrow-right-line text-white group-hover:ml-2 transition-all'></i>
          </button>

          <button 
            class='relative bg-black text-white font-space-mono text-base py-3 pl-6 pr-12 rounded-full hover:bg-black/75 transition-colors duration-300 hover:cursor-pointer uppercase group'>
            Button
            <i class='absolute ri-arrow-right-line text-white group-hover:-rotate-45 transition-all right-5'></i>
          </button>
          `"
        ></component-object>

        <component-object
          :name="'Button with Shadow Animation'"
          :code="`
          <button 
            class='bg-black shadow-lg shadow-black/20 text-white font-space-mono text-base py-3 px-6 rounded-full hover:bg-black/75 transition-all duration-300 hover:cursor-pointer hover:shadow-none hover:translate-y-1 uppercase'>
            Button
          </button>

          <button 
            class='bg-white shadow-lg shadow-black/20 text-black font-space-mono text-base py-3 px-6 rounded-full border border-black/20 hover:bg-black/5 transition-all hover:cursor-pointer hover:shadow-none hover:translate-y-1 uppercase'>
            Button
          </button>
          `"
        ></component-object>
      </component-section>

      <component-section
        name="Cards"
        description="Responsive card components for organizing content clearly. Built with accessibility in mind and designed for easy reuse and TailwindCSS-driven layout customization."
      ></component-section>
    </main>
  </div>
</template>
