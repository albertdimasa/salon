<template>
    <div class="flex flex-col gap-2 justify-center items-center h-screen">
        <p class="mb-2">Ini adalah beberapa halaman yang sudah dibuat</p>
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