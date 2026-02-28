<script setup>
import { RouterLink } from 'vue-router'
import ComponentCard from './ComponentCard.vue'
import SectionHeader from './SectionHeader.vue'
</script>

<template>
  <div class="section-container relative px-3">
    <SectionHeader
      title="Tailwind CSS Components"
      description="Browse a complete set of clean, reusable UI components built for modern frontend workflows with Tailwind CSS. "
    ></SectionHeader>

    <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-5">
      <router-link to="/">
        <ComponentCard
          title="Buttons"
          content="<button class='btn-primary uppercase'>Button</button>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Cards"
          content="<div class='p-3 rounded-lg border border-gray-200 flex flex-col gap-2 font-manrope'><h3 class='text-lg font-semibold'>Card Title</h3><p class='text-small opacity-75'>This is a sample card content.</p></div>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Inputs"
          content="<input type='text' class='input-box' placeholder='Input Field' />"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Text Areas"
          content="<textarea class='textarea-box' rows='4' placeholder='Text Area Field'></textarea>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Paginations"
          content="<nav class='flex items-center gap-1'>

  <!-- Prev -->
  <button class='w-9 h-9 flex items-center justify-center text-sm rounded border border-text-primary/50 bg-primary text-text-primary hover:border-avocado-500 hover:text-text-primary/70 transition-colors cursor-pointer'>
    &#8592;
  </button>

  <!-- Page 1 -->
  <button class='w-9 h-9 flex items-center justify-center text-xs rounded border border-text-primary/50 bg-primary text-text-primary hover:border-avocado-500 hover:text-text-primary/70 transition-colors cursor-pointer font-medium'>
    1
  </button>

  <!-- Page 2 (active) -->
  <button class='w-9 h-9 flex items-center justify-center text-xs rounded border border-avocado-400 bg-avocado-400 text-stone-950 cursor-default font-medium'>
    2
  </button>

  <!-- Page 3 -->
  <button class='w-9 h-9 flex items-center justify-center text-xs rounded border border-text-primary/50 bg-primary text-text-primary hover:border-avocado-500 hover:text-text-primary/70 transition-colors cursor-pointer font-medium'>
    3
  </button>

  <!-- Ellipsis -->
  <span class='w-9 h-9 flex items-center justify-center text-stone-600 text-xs'>···</span>

  <!-- Page 12 -->
  <button class='w-9 h-9 flex items-center justify-center text-xs rounded border border-text-primary/50 bg-primary text-text-primary hover:border-avocado-500 hover:text-text-primary/70 transition-colors cursor-pointer font-medium'>
    12
  </button>

  <!-- Next -->
  <button class='w-9 h-9 flex items-center justify-center text-sm rounded border border-text-primary/50 bg-primary text-text-primary hover:border-avocado-500 hover:text-text-primary/70 transition-colors cursor-pointer'>
    &#8594;
  </button>

</nav>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Badges"
          content="
          <div class='flex items-center gap-2'>
            <span class='rounded-sm bg-avocado-200 px-2.5 py-1 text-sm whitespace-nowrap text-avocado-700'>Badge</span>
            <span class='rounded-sm bg-avocado-600 px-2.5 py-1 text-sm whitespace-nowrap text-avocado-100'>Badge</span>
            <span class='rounded-sm bg-avocado-200 px-2.5 py-1 text-sm whitespace-nowrap text-avocado-700'><i class='ri-checkbox-circle-line'></i> Badge</span>
          </div>
            "
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Select Options"
          content="<select class='input-box'><option>Option 1</option><option>Option 2</option><option>Option 3</option></select>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Breadcrumbs"
          content="<ol class='flex items-center gap-1 text-sm text-gray-700'>
                      <li>
                        <a href='#' class='block transition-colors hover:text-text-primary text-small'> Category </a>
                      </li>
                      <i class='ri-arrow-right-s-line text-gray-500'></i>
                      <li>
                        <a href='#' class='block transition-colors hover:text-text-primary text-small'> Current Page </a>
                      </li>
                    </ol>"
        />
      </router-link>
    </div>
  </div>
</template>
