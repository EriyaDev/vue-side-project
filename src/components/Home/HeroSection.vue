<script setup></script>

<template>
  <div id="hero-section" class="w-full min-h-screen flex pt-40 relative">
    <div class="container mx-auto z-10">
      <div class="flex flex-col gap-2 lg:items-center">
        <div
          class="py-2 flex flex-row items-center gap-1 w-fit px-3 text-badge rounded-full border border-text-primary/10 shadow-sm shadow-text-secondary/5"
        >
          <div class="w-4 h-4 rounded-full bg-black"></div>
          Built for modern frontend
        </div>
        <h1 class="text-display text-text-primary font-medium">Build faster. Ship cleaner UI.</h1>

        <p class="text-body text-text-secondary lg:max-w-[50%] lg:text-center">
          A production-ready UI component library for React, Vue, and Tailwind. Clean by default,
          fully reusable, and designed to scale with your product.
        </p>
        <div class="flex flex-row items-center gap-4 mt-6">
          <button class="btn-primary uppercase">Browse Components</button>
          <button class="btn-secondary uppercase">View Docs</button>
        </div>
      </div>
    </div>
    <div class="absolute inset-0 z-0 bg-dashed-line"></div>
    <div class="absolute inset-0 -z-10 bg-gradient"></div>
  </div>
</template>
