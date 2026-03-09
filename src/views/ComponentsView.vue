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
            to="/components#Text-Areas"
            >Text Areas</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Pagination"
            >Pagination</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Badges"
            >Badges</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Select-Options"
            >Select Options</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all hover:pl-1"
            to="/components#Breadcrumbs"
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
          :name="'Default Input'"
          :code="`
          <div class='flex flex-col gap-2 w-full max-w-sm'>
            <label for='basic-input' class='font-grotesk font-semibold text-gray-800 text-sm'>Username</label>
            <input type='text' id='basic-input' class='w-full px-4 py-3 rounded-lg border border-black/10 focus:outline-none focus:border-avocado-500 focus:ring-1 focus:ring-avocado-500 transition-all font-manrope placeholder-black/30' placeholder='Enter username'>
          </div>
          `"
        ></component-object>

        <component-object
          :name="'Inputs with Icon'"
          :code="`
          <div class='flex flex-col gap-2 w-full max-w-sm'>
            <label for='left-icon-input' class='font-grotesk font-semibold text-gray-800 text-sm'>Email Address</label>
            <div class='relative'>
              <div class='absolute left-4 top-1/2 -translate-y-1/2 pointer-events-none text-gray-500 flex items-center justify-center'>
                <i class='ri-mail-line text-lg'></i>
              </div>
              <input type='email' id='left-icon-input' class='w-full pl-11 pr-4 py-3 rounded-lg border border-black/10 focus:outline-none focus:border-avocado-500 focus:ring-1 focus:ring-avocado-500 transition-all font-manrope placeholder-black/30' placeholder='you@example.com'>
            </div>
          </div>

          <div class='flex flex-col gap-2 w-full max-w-sm'>
            <label for='right-icon-input' class='font-grotesk font-semibold text-gray-800 text-sm'>Search</label>
            <div class='relative'>
              <input type='text' id='right-icon-input' class='w-full pl-4 pr-11 py-3 rounded-lg border border-black/10 focus:outline-none focus:border-avocado-500 focus:ring-1 focus:ring-avocado-500 transition-all font-manrope placeholder-black/30' placeholder='Search items...'>
              <div class='absolute right-4 top-1/2 -translate-y-1/2 text-gray-500 flex items-center justify-center hover:text-black transition-colors cursor-pointer'>
                <i class='ri-search-line text-lg'></i>
              </div>
            </div>
          </div>
          `"
        ></component-object>
      </component-section>

      <component-section
        id="Text-Areas"
        name="Text Areas"
        description="Accessible textarea components for longer user input. Responsive, reusable, and fully customizable with TailwindCSS utilities to match any production-ready form design."
      >
        <component-object
          :name="'Default Text Area'"
          :code="`
          <div class='flex flex-col gap-2 w-full max-w-sm'>
            <label for='message' class='font-grotesk font-semibold text-gray-800 text-sm'>Your Message</label>
            <textarea id='message' rows='4' class='w-full px-4 py-3 rounded-lg border border-black/10 focus:outline-none focus:border-avocado-500 focus:ring-1 focus:ring-avocado-500 transition-all font-manrope placeholder-black/30' placeholder='Write your message here...'></textarea>
          </div>
          `"
        ></component-object>
      </component-section>

      <component-section
        id="Pagination"
        name="Pagination"
        description="Responsive pagination components for navigating large datasets. Accessible, reusable, and easily styled with TailwindCSS to integrate seamlessly into any application layout."
      >
        <component-object
          :name="'Simple Pagination'"
          :code="`
          <div class='flex items-center gap-2'>
            <button class='w-10 h-10 flex items-center justify-center rounded-lg border border-black/10 text-gray-600 hover:bg-avocado-500 hover:text-black hover:border-avocado-500 transition-all'>
              <i class='ri-arrow-left-s-line'></i>
            </button>
            <button class='w-10 h-10 flex items-center justify-center rounded-lg bg-avocado-500 text-black font-semibold transition-all shadow-sm'>
              1
            </button>
            <button class='w-10 h-10 flex items-center justify-center rounded-lg border border-black/10 text-gray-600 hover:bg-avocado-500 hover:text-black hover:border-avocado-500 transition-all'>
              2
            </button>
            <button class='w-10 h-10 flex items-center justify-center rounded-lg border border-black/10 text-gray-600 hover:bg-avocado-500 hover:text-black hover:border-avocado-500 transition-all'>
              3
            </button>
            <button class='w-10 h-10 flex items-center justify-center rounded-lg border border-black/10 text-gray-600 hover:bg-avocado-500 hover:text-black hover:border-avocado-500 transition-all'>
              <i class='ri-arrow-right-s-line'></i>
            </button>
          </div>
          `"
        ></component-object>
      </component-section>

      <component-section
        id="Badges"
        name="Badges"
        description="Small, reusable badge components for labels, statuses, and counts. Accessible, responsive, and customizable using TailwindCSS for consistent visual communication."
      >
        <component-object
          :name="'Status Badges'"
          :code="`
          <div class='flex flex-wrap gap-3'>
            <span class='px-3 py-1 bg-avocado-500 text-black font-space-mono text-xs rounded-full uppercase tracking-wider font-semibold'>Active</span>
            <span class='px-3 py-1 bg-gray-100 text-gray-600 font-space-mono text-xs rounded-full border border-gray-200 uppercase tracking-wider font-semibold'>Inactive</span>
            <span class='px-3 py-1 bg-avocado-500/20 text-avocado-700 font-space-mono text-xs rounded-full border border-avocado-500/30 uppercase tracking-wider font-semibold'>New</span>
            <span class='px-3 py-1 bg-black text-white font-space-mono text-xs rounded-full uppercase tracking-wider font-semibold'>Premium</span>
          </div>
          `"
        ></component-object>
      </component-section>

      <component-section
        id="Select-Options"
        name="Select Options"
        description="Accessible select components with consistent styling and interaction states. Reusable and responsive, with full TailwindCSS customization for modern form experiences."
      >
        <component-object
          :name="'Stylized Select'"
          :code="`
          <div class='flex flex-col gap-2 w-full max-w-sm'>
            <label for='options' class='font-grotesk font-semibold text-gray-800 text-sm'>Select an option</label>
            <div class='relative'>
              <select id='options' class='w-full px-4 py-3 rounded-lg border border-black/10 focus:outline-none focus:border-avocado-500 focus:ring-1 focus:ring-avocado-500 appearance-none bg-white font-manrope text-gray-800 transition-all hover:cursor-pointer hover:border-black/30'>
                <option value='' disabled selected>Choose a plan...</option>
                <option value='basic'>Basic Plan</option>
                <option value='pro'>Pro Plan</option>
                <option value='enterprise'>Enterprise Plan</option>
              </select>
              <div class='absolute right-4 top-1/2 -translate-y-1/2 pointer-events-none text-gray-500 flex items-center justify-center'>
                <i class='ri-arrow-down-s-line text-lg'></i>
              </div>
            </div>
          </div>
          `"
        ></component-object>
      </component-section>

      <component-section
        id="Breadcrumbs"
        name="Breadcrumbs"
        description="Accessible breadcrumb components for showing navigation hierarchy. Responsive, reusable, and easily customizable with TailwindCSS for clear and structured user navigation."
      >
        <component-object
          :name="'Basic Breadcrumbs'"
          :code="`
          <nav class='flex items-center text-sm font-manrope text-gray-500 gap-2'>
            <a href='#' class='hover:text-avocado-600 hover:underline underline-offset-4 transition-all'>Home</a>
            <i class='ri-arrow-right-s-line text-black/30'></i>
            <a href='#' class='hover:text-avocado-600 hover:underline underline-offset-4 transition-all'>Products</a>
            <i class='ri-arrow-right-s-line text-black/30'></i>
            <span class='text-gray-900 font-semibold'>Current Page</span>
          </nav>
          `"
        ></component-object>
      </component-section>
    </main>
  </div>
</template>
