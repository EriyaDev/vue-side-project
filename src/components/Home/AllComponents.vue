<script setup></script>

<template>
  <div class="container mx-auto section-header">
    <h1 class="medium-heading font-semibold">Tailwind CSS Components</h1>
    <p class="text-body max-w-[50%] text-center">
      Browse a complete set of clean, reusable UI components built for modern frontend workflows
      with Tailwind CSS.
    </p>
  </div>

  <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-5">
    <div class="w-full h-64 bg-secondary border border-text-secondary/30 rounded-lg">
      <div class="h-10 border-b border-text-secondary/30 rounded mb-3 py-1 px-3">
        <h4 class="small-heading font-semibold leading-none">Button</h4>
      </div>
      <div class="w-full flex justify-center items-center">
        <button class="btn-primary uppercase">Button</button>
      </div>
    </div>
  </div>
</template>
