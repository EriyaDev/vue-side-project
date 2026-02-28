<script setup>
import { RouterLink } from 'vue-router'
import ComponentCard from './ComponentCard.vue'
import SectionHeader from './SectionHeader.vue'
</script>

<template>
  <div class="section-container relative px-3">
    <SectionHeader
      title="Tailwind CSS Sections"
      description="Browse a complete set of clean, reusable UI sections built for modern frontend workflows with Tailwind CSS. "
    ></SectionHeader>

    <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-5">
      <router-link to="/">
        <ComponentCard title="Hero Sections" content="<h2 class='text'>COMING SOON</h2>" />
      </router-link>
      <router-link to="/">
        <ComponentCard title="About Sections" content="<h2 class='text'>COMING SOON</h2>" />
      </router-link>
      <router-link to="/">
        <ComponentCard title="Testimonial Sections" content="<h2 class='text'>COMING SOON</h2>" />
      </router-link>
      <router-link to="/">
        <ComponentCard title="FAQ Sections" content="<h2 class='text'>COMING SOON</h2>" />
      </router-link>
    </div>
  </div>
</template>
