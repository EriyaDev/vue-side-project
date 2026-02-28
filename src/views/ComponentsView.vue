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

        <div class="bg-white border border-gray-200 w-full lg:w-[60%] rounded-xl overflow-hidden">
          <!-- Header -->
          <div class="flex items-center justify-between px-5 py-3 border-b border-gray-200">
            <div>
              <p class="text-sm font-semibold text-gray-900">Base</p>
              <p class="text-xs text-gray-400">markmead</p>
            </div>
            <div class="flex items-center gap-3">
              <div class="flex gap-1.5">
                <button
                  class="px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  Mobile
                </button>
                <button
                  class="px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  SM
                </button>
                <button
                  class="px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  MD
                </button>
                <button
                  class="px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  LG
                </button>
                <button
                  class="px-3 py-1 text-xs font-medium rounded-md bg-gray-900 text-white border border-gray-900"
                >
                  Full
                </button>
              </div>
              <div class="flex gap-1.5">
                <button
                  class="flex items-center gap-1.5 px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  <svg
                    class="w-3.5 h-3.5"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                  >
                    <path d="M3 5h18M3 12h18M3 19h18" />
                  </svg>
                  LTR
                </button>
                <button
                  class="flex items-center gap-1.5 px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  <svg
                    class="w-3.5 h-3.5"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                  >
                    <circle cx="12" cy="12" r="3" />
                    <path d="M2 12s3-7 10-7 10 7 10 7-3 7-10 7-10-7-10-7z" />
                  </svg>
                  Preview
                </button>
                <button
                  class="flex items-center gap-1.5 px-3 py-1 text-xs font-medium rounded-md border border-gray-200 text-gray-600 hover:bg-gray-50 transition"
                >
                  <svg
                    class="w-3.5 h-3.5"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                  >
                    <rect x="9" y="9" width="13" height="13" rx="2" />
                    <path d="M5 15H4a2 2 0 01-2-2V4a2 2 0 012-2h9a2 2 0 012 2v1" />
                  </svg>
                  Copy
                </button>
              </div>
            </div>
          </div>

          <!-- Body -->
          <div class="flex items-center justify-center py-16 px-6">
            <div class="flex flex-col gap-1.5 w-72">
              <label for="email" class="text-sm font-medium text-gray-700">Email</label>
              <input
                type="email"
                id="email"
                class="w-full rounded-md border border-gray-300 px-3 py-2 text-sm text-gray-900 shadow-sm outline-none focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500/20 transition"
                placeholder=""
              />
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>
