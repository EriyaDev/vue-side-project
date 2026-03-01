<script setup></script>

<template>
  <div class="min-h-screen grid grid-cols-1 lg:grid-cols-[250px_1fr]">
    <!-- Sidebar -->
    <aside class="hidden lg:block bg-gray-50 border-r border-gray-200 p-4 h-full">
      <nav class="space-y-2 mt-20">
        <!-- Navigation items -->
        <h2 class="text-body font-semibold">COMPONENTS</h2>
        <div class="flex flex-col gap-1.5 mt-4">
          <router-link class="text-small hover:opacity-70 transition-all" to="/components#button"
            >Buttons</router-link
          >
          <router-link class="text-small hover:opacity-70 transition-all" to="/components#card"
            >Cards</router-link
          >
          <router-link class="text-small hover:opacity-70 transition-all" to="/components#input"
            >Inputs</router-link
          >
          <router-link class="text-small hover:opacity-70 transition-all" to="/components#textarea"
            >Text Areas</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all"
            to="/components#pagination"
            >Pagination</router-link
          >
          <router-link class="text-small hover:opacity-70 transition-all" to="/components#badge"
            >Badges</router-link
          >
          <router-link class="text-small hover:opacity-70 transition-all" to="/components#select"
            >Select Options</router-link
          >
          <router-link
            class="text-small hover:opacity-70 transition-all"
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

        <div class="w-full lg:max-w-[60%] border border-text-primary/10 rounded-2xl">
          <div
            class="w-full border-b border-b-text-primary/10 p-4 justify-between items-center flex gap-4"
          >
            <p class="text-body font-medium">Button Primary</p>

            <div class="flex gap-2">
              <button
                class="flex items-center gap-2 border border-text-primary/10 rounded-lg py-0.5 px-2"
              >
                <i class="ri-code-s-slash-line"></i>
                <p class="text-small text-text-primary/70">Code</p>
              </button>
              <button
                class="flex items-center gap-2 border border-text-primary/10 rounded-lg py-0.5 px-2"
              >
                <i class="ri-file-copy-line"></i>
                <p class="text-small text-text-primary/70">Copy</p>
              </button>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>
