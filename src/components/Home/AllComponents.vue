<script setup>
import { RouterLink } from 'vue-router'
import ComponentCard from './ComponentCard.vue'
import SectionHeader from './SectionHeader.vue'
</script>

<template>
  <div class="section-container relative">
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
          content="<div class='card-primary'><h3 class='card-title'>Card Title</h3><p class='card-content'>This is a sample card content.</p></div>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Inputs"
          content="<input type='text' class='input-primary' placeholder='Input Field' />"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Text Areas"
          content="<textarea class='textarea-primary' placeholder='Text Area Field'></textarea>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Paginations"
          content="<div class='pagination-container'><button class='pagination-btn'>1</button><button class='pagination-btn'>2</button><button class='pagination-btn'>3</button></div>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard title="Badges" content="<span class='badge-primary'>Badge</span>" />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Select Options"
          content="<select class='select-primary'><option>Option 1</option><option>Option 2</option><option>Option 3</option></select>"
        />
      </router-link>
      <router-link to="/">
        <ComponentCard
          title="Breadcrumbs"
          content="<div class='breadcrumb-container'><span class='breadcrumb-item'>Home</span><span class='breadcrumb-separator'>/</span><span class='breadcrumb-item'>Category</span><span class='breadcrumb-separator'>/</span><span class='breadcrumb-item active'>Current Page</span></div>"
        />
      </router-link>
    </div>
  </div>
</template>
