<template>
  <div class="min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800 px-4 py-8">
    <div class="w-full max-w-md">
      <!-- Card Container -->
      <UCard class="shadow-xl">
        <!-- Header -->
        <template #header>
          <div class="text-center">
            <div class="inline-flex items-center justify-center w-16 h-16 bg-primary-100 dark:bg-primary-900/30 rounded-full mb-4">
              <UIcon name="i-heroicons-envelope-open" class="w-8 h-8 text-primary-500" />
            </div>
            <h1 class="text-3xl font-bold text-gray-900 dark:text-white mb-2">
              Verifikasi Email
            </h1>
            <p class="text-gray-600 dark:text-gray-400">
              Kami telah mengirim email verifikasi ke
            </p>
            <p class="text-primary-500 dark:text-primary-400 font-medium mt-1">
              {{ email }}
            </p>
          </div>
        </template>

        <!-- Content -->
        <div class="space-y-6">
          <!-- Instructions -->
          <div class="bg-gray-50 dark:bg-gray-800/50 rounded-lg p-4 space-y-3">
            <div class="flex items-start">
              <UIcon name="i-heroicons-information-circle" class="w-5 h-5 text-primary-500 mt-0.5 mr-3 flex-shrink-0" />
              <p class="text-sm text-gray-700 dark:text-gray-300">
                Silakan cek inbox atau folder spam email Anda dan klik link verifikasi yang kami kirimkan.
              </p>
            </div>
          </div>

          <!-- Resend Button -->
          <div class="text-center">
            <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
              Tidak menerima email?
            </p>
            <UButton
              variant="outline"
              size="lg"
              :loading="loading"
              @click="resendEmail"
              class="w-full"
            >
              <UIcon name="i-heroicons-arrow-path" class="w-4 h-4 mr-2" />
              Kirim Ulang Email
            </UButton>
          </div>

          <!-- Success Message -->
          <UAlert
            v-if="success"
            color="success"
            variant="soft"
            title="Email terkirim!"
            description="Silakan cek email Anda kembali."
            icon="i-heroicons-check-circle"
          />
        </div>

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
// Bisa diambil dari route query atau store
const email = ref('user@example.com')

const loading = ref(false)
const success = ref(false)

const resendEmail = async () => {
  loading.value = true
  success.value = false
  
  // Simulasi API call
  await new Promise(resolve => setTimeout(resolve, 1500))
  
  console.log('Resending verification email to:', email.value)
  
  loading.value = false
  success.value = true
  
  // Hide success message after 3 seconds
  setTimeout(() => {
    success.value = false
  }, 3000)
}
</script>
