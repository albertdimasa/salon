<template>
  <div class="min-h-screen flex items-center justify-center bg-linear-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800 px-4 py-8">
    <!-- Back to Home Button -->
    <div class="absolute top-4 left-4">
      <NuxtLink
        to="/"
        class="inline-flex items-center px-4 py-2 text-sm text-gray-600 dark:text-gray-400 hover:text-primary-500 dark:hover:text-primary-400 transition-colors rounded-lg hover:bg-white/50 dark:hover:bg-gray-800/50"
      >
        <UIcon name="i-heroicons-home" class="w-5 h-5 mr-2" />
        Kembali ke Beranda
      </NuxtLink>
    </div>

    <!-- Dark Mode Toggle -->
    <div class="absolute top-4 right-4">
      <ThemeToggle />
    </div>

    <!-- Main Content -->
    <div class="w-full max-w-md">
      <slot />
    </div>
  </div>
</template>
