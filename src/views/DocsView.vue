<script setup></script>

<template>
  <div class="min-h-screen grid grid-cols-1 lg:grid-cols-[250px_1fr] grid-rows-[auto_1fr]">
    <!-- Header (spans full width on all screens) -->
    <header class="lg:col-span-2 bg-white border-b border-gray-200 p-4">
      <div class="flex items-center justify-between">
        <!-- Mobile menu button -->
        <button class="lg:hidden p-2">
          <svg class="w-6 h-6">...</svg>
        </button>
        <h1 class="text-xl font-semibold">Dashboard</h1>
        <div class="flex items-center space-x-4">
          <!-- User profile, notifications, etc. -->
        </div>
      </div>
    </header>

    <!-- Sidebar -->
    <aside class="hidden lg:block bg-gray-50 border-r border-gray-200 p-4">
      <nav class="space-y-2">
        <!-- Navigation items -->
      </nav>
    </aside>

    <!-- Main content area -->
    <main class="p-6 overflow-auto">
      <!-- Dashboard content -->
      <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-6">
        <!-- Cards, charts, etc. -->
      </div>
    </main>
  </div>
</template>
