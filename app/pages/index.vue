<template>
    <div class="relative flex flex-col gap-2 justify-center items-center h-screen bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800">
        <!-- Dark Mode Toggle -->
        <div class="absolute top-4 right-4">
            <ThemeToggle />
        </div>
        
        <p class="mb-2 text-gray-900 dark:text-white">Ini adalah beberapa halaman yang sudah dibuat</p>
        <div class="flex gap-2">
            <NuxtLink to="/auth/login" class="transition-transform duration-200 hover:scale-110">
                <UButton size="lg">
                    Login
                </UButton>
            </NuxtLink>
            <NuxtLink to="/auth/register" class="transition-transform duration-200 hover:scale-110">
                <UButton size="lg">
                    Register
                </UButton>
            </NuxtLink>
            <NuxtLink to="/auth/verify-email" class="transition-transform duration-200 hover:scale-110">
                <UButton size="lg">
                    Verify Email
                </UButton>
            </NuxtLink>
            <NuxtLink to="/auth/forgot-password" class="transition-transform duration-200 hover:scale-110">
                <UButton size="lg">
                    Forgot Password
                </UButton>
            </NuxtLink>
        </div>
    </div>
</template>
<!-- <script setup>
definePageMeta({
  layout: 'auth'
})
</script> -->