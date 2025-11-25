<template>
  <div class="min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800 px-4 py-8">
    <div class="w-full max-w-md">
      <!-- Card Container -->
      <UCard class="shadow-xl">
        <!-- Header -->
        <template #header>
          <div class="text-center">
            <div class="inline-flex items-center justify-center w-16 h-16 bg-primary-100 dark:bg-primary-900/30 rounded-full mb-4">
              <UIcon name="i-heroicons-key" class="w-8 h-8 text-primary-500" />
            </div>
            <h1 class="text-3xl font-bold text-gray-900 dark:text-white mb-2">
              Lupa Password?
            </h1>
            <p class="text-gray-600 dark:text-gray-400">
              Masukkan email Anda untuk reset password
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
              class="w-full"
            />
          </UFormGroup>

          <!-- Submit Button -->
          <UButton
            type="submit"
            block
            size="lg"
            :loading="loading"
            class="shadow-lg hover:shadow-xl transition-shadow"
          >
            Kirim Link Reset
          </UButton>

          <!-- Success Message -->
          <UAlert
            v-if="success"
            color="success"
            variant="soft"
            title="Email terkirim!"
            description="Silakan cek email Anda untuk link reset password."
            icon="i-heroicons-check-circle"
          />
        </UForm>

        <!-- Footer -->
        <template #footer>
          <div class="text-center">
            <NuxtLink
              to="/auth/login"
              class="inline-flex items-center text-sm text-gray-600 dark:text-gray-400 hover:text-primary-500 dark:hover:text-primary-400 transition-colors"
            >
              <UIcon name="i-heroicons-arrow-left" class="w-4 h-4 mr-2" />
              Kembali ke Login
            </NuxtLink>
          </div>
        </template>
      </UCard>
    </div>
  </div>
</template>

<script setup lang="ts">
const state = reactive({
  email: ''
})

const loading = ref(false)
const success = ref(false)

const onSubmit = async () => {
  loading.value = true
  success.value = false
  
  // Simulasi API call
  await new Promise(resolve => setTimeout(resolve, 1500))
  
  console.log('Forgot password for:', state.email)
  
  loading.value = false
  success.value = true
  
  // Reset form after 3 seconds
  setTimeout(() => {
    success.value = false
    state.email = ''
  }, 3000)
}
</script>
