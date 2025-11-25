<template>
  <div class="min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800 px-4 py-8">
    <div class="w-full max-w-md">
      <!-- Card Container -->
      <UCard class="shadow-xl">
        <!-- Header -->
        <template #header>
          <div class="text-center">
            <h1 class="text-3xl font-bold text-gray-900 dark:text-white mb-2">
              Buat Akun Baru
            </h1>
            <p class="text-gray-600 dark:text-gray-400">
              Daftar untuk memulai
            </p>
          </div>
        </template>

        <!-- Form -->
        <UForm :state="state" @submit="onSubmit" class="space-y-5">
          <!-- Name Field -->
          <UFormGroup label="Nama Lengkap" name="name" required>
            <UInput
              v-model="state.name"
              type="text"
              placeholder="Nama lengkap Anda"
              icon="i-heroicons-user"
              size="lg"
              class="w-full"
            />
          </UFormGroup>

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

          <!-- Password Field -->
          <UFormGroup label="Password" name="password" required>
            <UInput
              v-model="state.password"
              type="password"
              placeholder="Minimal 8 karakter"
              icon="i-heroicons-lock-closed"
              size="lg"
              class="w-full"
            />
          </UFormGroup>

          <!-- Confirm Password Field -->
          <UFormGroup label="Konfirmasi Password" name="confirmPassword" required>
            <UInput
              v-model="state.confirmPassword"
              type="password"
              placeholder="Ulangi password"
              icon="i-heroicons-lock-closed"
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
            class="shadow-lg hover:shadow-xl transition-shadow mt-6"
          >
            Daftar
          </UButton>
        </UForm>

        <!-- Footer -->
        <template #footer>
          <div class="text-center text-sm text-gray-600 dark:text-gray-400">
            Sudah punya akun?
            <NuxtLink
              to="/auth/login"
              class="text-primary-500 hover:text-primary-600 dark:text-primary-400 dark:hover:text-primary-300 font-medium transition-colors"
            >
              Masuk di sini
            </NuxtLink>
          </div>
        </template>
      </UCard>
    </div>
  </div>
</template>

<script setup lang="ts">
const state = reactive({
  name: '',
  email: '',
  password: '',
  confirmPassword: ''
})

const loading = ref(false)

const onSubmit = async () => {
  // Validasi password match
  if (state.password !== state.confirmPassword) {
    alert('Password tidak cocok!')
    return
  }

  loading.value = true
  
  // Simulasi API call
  await new Promise(resolve => setTimeout(resolve, 1500))
  
  console.log('Register data:', state)
  
  loading.value = false
  
  // Redirect ke verify email atau login
  // navigateTo('/auth/verify-email')
}
</script>
