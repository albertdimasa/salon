<template>
  <UCard class="shadow-xl">
        <!-- Header -->
        <template #header>
          <div class="text-center">
            <h1 class="text-3xl font-bold text-gray-900 dark:text-white mb-2">
              Selamat Datang
            </h1>
            <p class="text-gray-600 dark:text-gray-400">
              Masuk ke akun Anda
            </p>
          </div>
        </template>

        <!-- Form -->
        <UForm :state="state" @submit="onSubmit" class="space-y-6">
          <!-- Email Field -->
          <UFormGroup label="Email" name="email" required>
            <UInput
              v-model="state.email"
              type="email"
              placeholder="nama@email.com"
              icon="i-heroicons-envelope"
              size="lg"
              class="w-full mb-2"
            />
          </UFormGroup>

          <!-- Password Field -->
          <UFormGroup label="Password" name="password" required>
            <UInput
              v-model="state.password"
              type="password"
              placeholder="Masukkan password"
              icon="i-heroicons-lock-closed"
              size="lg"
              class="w-full mb-3"
            />
          </UFormGroup>

          <!-- Forgot Password Link -->
          <div class="flex justify-end">
            <NuxtLink
              to="/auth/forgot-password"
              class="text-sm text-primary-500 hover:text-primary-600 dark:text-primary-400 dark:hover:text-primary-300 transition-colors"
            >
              Lupa password?
            </NuxtLink>
          </div>

          <!-- Submit Button -->
          <UButton
            type="submit"
            block
            size="lg"
            :loading="loading"
            class="shadow-lg hover:shadow-xl transition-shadow"
          >
            Masuk
          </UButton>
        </UForm>

        <!-- Footer -->
        <template #footer>
          <div class="text-center text-sm text-gray-600 dark:text-gray-400">
            Belum punya akun?
            <NuxtLink
              to="/auth/register"
              class="text-primary-500 hover:text-primary-600 dark:text-primary-400 dark:hover:text-primary-300 font-medium transition-colors"
            >
              Daftar sekarang
            </NuxtLink>
          </div>
        </template>
  </UCard>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'auth'
})

const state = reactive({
  email: '',
  password: ''
})

const loading = ref(false)

const onSubmit = async () => {
  loading.value = true
  
  // Simulasi API call
  await new Promise(resolve => setTimeout(resolve, 1500))
  
  console.log('Login data:', state)
  
  loading.value = false
  
  // Redirect atau handle login success
  // navigateTo('/dashboard')
}
</script>
