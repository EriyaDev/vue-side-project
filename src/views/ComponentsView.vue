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
            to="/components#Buttons"
            >Buttons</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Cards"
            >Cards</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Inputs"
            >Inputs</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#TextAreas"
            >Text Areas</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Pagination"
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
        id="Buttons"
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
        id="Cards"
        name="Cards"
        description="Responsive card components for organizing content clearly. Built with accessibility in mind and designed for easy reuse and TailwindCSS-driven layout customization."
      >
        <component-object
          :name="'Product Card'"
          :code="`
          <div class='w-full max-w-sm bg-white rounded-xl border border-black/10 overflow-hidden group'>
          <div class='relative w-full h-48 overflow-hidden'>
            <img class='w-full h-full object-cover group-hover:scale-110 transition-all' src='https://images.unsplash.com/photo-1491553895911-0055eca6402d?q=80&w=880&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' alt='Image'>
          </div>
            <div class='p-6'>
              <h3 class='text-xl font-grotesk font-semibold text-gray-800 mb-2'>Product Name</h3>
              <p class='text-black/55 font-manrope mb-4'>Product description goes here. It can be a few sentences describing the product.</p>
              <div class='flex items-center justify-between'>
                <span class='font-grotesk text-2xl font-bold text-gray-900'>$99.99</span>
                <button class='px-4 py-2 font-grotesk bg-avocado-500 text-black rounded-lg hover:brightness-95 transition-all'>
                  Add to Cart
                </button>
              </div>
            </div>
          </div>
          `"
        ></component-object>

        <component-object
          :name="'Testimonial Card'"
          :code="`
<div class='max-w-sm rounded-lg border border-black/10 bg-white p-5 transition-all group flex flex-col gap-4 hover:border-avocado-500'>
  <i class='ri-double-quotes-l text-4xl text-avocado-700'></i>
  <p class='font-manrope line-clamp-3 text-black/55'>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod.
  </p>
  <div class='flex w-full flex-row items-center gap-3 pt-2'>
    <img
      src='https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?w=40&h=40&fit=crop&crop=face'
      alt='Profile Icon'
      class='w-11 h-11 rounded-full object-cover'
    />
    <div>
      <h6 class='font-grotesk font-bold'>JANE DOE</h6>
      <div class='flex flex-row items-center gap-1'>
        <i class='ri-star-fill text-yellow-400'></i>
        <p class='font-grotesk'>10.0</p>
      </div>
    </div>
  </div>
</div>
          `"
        ></component-object>
      </component-section>

      <component-section
        id="Inputs"
        name="Inputs"
        description="Form input components supporting validation, focus states, and accessibility standards. Easily reusable and customizable using TailwindCSS for consistent, responsive form interfaces."
      >
        <component-object
          :name="'Product Card'"
          :code="`
          <div class='w-full max-w-sm bg-white rounded-xl border border-black/10 overflow-hidden group'>
          <div class='relative w-full h-48 overflow-hidden'>
            <img class='w-full h-full object-cover group-hover:scale-110 transition-all' src='https://images.unsplash.com/photo-1491553895911-0055eca6402d?q=80&w=880&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' alt='Image'>
          </div>
            <div class='p-6'>
              <h3 class='text-xl font-grotesk font-semibold text-gray-800 mb-2'>Product Name</h3>
              <p class='text-black/55 font-manrope mb-4'>Product description goes here. It can be a few sentences describing the product.</p>
              <div class='flex items-center justify-between'>
                <span class='font-grotesk text-2xl font-bold text-gray-900'>$99.99</span>
                <button class='px-4 py-2 font-grotesk bg-avocado-500 text-black rounded-lg hover:brightness-95 transition-all'>
                  Add to Cart
                </button>
              </div>
            </div>
          </div>
          `"
        ></component-object>
      </component-section>
    </main>
  </div>
</template>
