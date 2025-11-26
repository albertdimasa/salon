<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800">
    <!-- Navigation -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-white/80 dark:bg-gray-900/80 backdrop-blur-lg border-b border-gray-200 dark:border-gray-800">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
          <!-- Logo -->
          <div class="flex items-center space-x-2">
            <UIcon name="i-heroicons-scissors" class="w-8 h-8 text-primary-500" />
            <span class="text-xl font-bold text-gray-900 dark:text-white">Salon MS</span>
          </div>

          <!-- Navigation Links -->
          <div class="hidden md:flex items-center space-x-8">
            <a href="#features" class="text-gray-600 dark:text-gray-300 hover:text-primary-500 dark:hover:text-primary-400 transition-colors">Fitur</a>
            <a href="#pricing" class="text-gray-600 dark:text-gray-300 hover:text-primary-500 dark:hover:text-primary-400 transition-colors">Harga</a>
            <a href="#about" class="text-gray-600 dark:text-gray-300 hover:text-primary-500 dark:hover:text-primary-400 transition-colors">Tentang</a>
          </div>

          <!-- CTA Buttons -->
          <div class="flex items-center space-x-4">
            <ThemeToggle />
            <NuxtLink to="/auth/login">
              <UButton variant="ghost" color="secondary">Masuk</UButton>
            </NuxtLink>
            <NuxtLink to="/auth/register">
              <UButton>Daftar Gratis</UButton>
            </NuxtLink>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="pt-32 pb-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <div class="text-center">
          <div class="inline-flex items-center px-4 py-2 bg-primary-100 dark:bg-primary-900/30 rounded-full mb-6">
            <UIcon name="i-heroicons-sparkles" class="w-5 h-5 text-primary-500 mr-2" />
            <span class="text-sm font-medium text-primary-700 dark:text-primary-300">Solusi Terbaik untuk Bisnis Salon Anda</span>
          </div>
          
          <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 dark:text-white mb-6">
            Kelola Salon Anda<br />
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary-500 to-purple-600">Lebih Mudah & Efisien</span>
          </h1>
          
          <p class="text-xl text-gray-600 dark:text-gray-300 mb-8 max-w-3xl mx-auto">
            Sistem manajemen salon all-in-one dengan POS terintegrasi yang membantu Anda mengelola booking, pelanggan, inventori, dan keuangan dalam satu platform modern.
          </p>

          <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
            <NuxtLink to="/auth/register">
              <UButton size="xl" class="shadow-lg hover:shadow-xl transition-shadow">
                <UIcon name="i-heroicons-rocket-launch" class="w-5 h-5 mr-2" />
                Mulai Gratis Sekarang
              </UButton>
            </NuxtLink>
            <UButton size="xl" variant="outline" color="secondary">
              <UIcon name="i-heroicons-play-circle" class="w-5 h-5 mr-2" />
              Lihat Demo
            </UButton>
          </div>

          <p class="text-sm text-gray-500 dark:text-gray-400 mt-4">
            ✨ Gratis 14 hari • Tidak perlu kartu kredit • Setup dalam 5 menit
          </p>
        </div>

        <!-- Hero Image/Illustration -->
        <div class="mt-16 relative">
          <div class="absolute inset-0 bg-gradient-to-r from-primary-500/20 to-purple-600/20 blur-3xl"></div>
          <div class="relative bg-white dark:bg-gray-800 rounded-2xl shadow-2xl p-8 border border-gray-200 dark:border-gray-700">
            <div class="grid grid-cols-3 gap-4">
              <div class="bg-gradient-to-br from-primary-50 to-primary-100 dark:from-primary-900/20 dark:to-primary-800/20 rounded-lg p-6 text-center">
                <UIcon name="i-heroicons-calendar-days" class="w-12 h-12 text-primary-500 mx-auto mb-2" />
                <p class="text-sm font-medium text-gray-700 dark:text-gray-300">Booking Online</p>
              </div>
              <div class="bg-gradient-to-br from-indigo-50 to-indigo-100 dark:from-indigo-900/20 dark:to-indigo-800/20 rounded-lg p-6 text-center">
                <UIcon name="i-heroicons-computer-desktop" class="w-12 h-12 text-indigo-500 mx-auto mb-2" />
                <p class="text-sm font-medium text-gray-700 dark:text-gray-300">Sistem POS</p>
              </div>
              <div class="bg-gradient-to-br from-pink-50 to-pink-100 dark:from-pink-900/20 dark:to-pink-800/20 rounded-lg p-6 text-center">
                <UIcon name="i-heroicons-chart-bar" class="w-12 h-12 text-pink-500 mx-auto mb-2" />
                <p class="text-sm font-medium text-gray-700 dark:text-gray-300">Laporan & Analitik</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-20 px-4 sm:px-6 lg:px-8 bg-white dark:bg-gray-900">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">Fitur Lengkap untuk Salon Modern</h2>
          <p class="text-xl text-gray-600 dark:text-gray-300">Semua yang Anda butuhkan untuk menjalankan salon yang sukses</p>
        </div>

        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Feature 1 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-primary-100 dark:bg-primary-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-calendar-days" class="w-6 h-6 text-primary-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Booking Online 24/7</h3>
            <p class="text-gray-600 dark:text-gray-300">Pelanggan dapat booking kapan saja melalui website atau aplikasi mobile</p>
          </div>

          <!-- Feature 2 - POS System -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-indigo-100 dark:bg-indigo-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-computer-desktop" class="w-6 h-6 text-indigo-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Sistem POS Terintegrasi</h3>
            <p class="text-gray-600 dark:text-gray-300">Point of Sale modern untuk transaksi cepat dengan berbagai metode pembayaran</p>
          </div>

          <!-- Feature 3 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-purple-100 dark:bg-purple-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-users" class="w-6 h-6 text-purple-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Database Pelanggan</h3>
            <p class="text-gray-600 dark:text-gray-300">Simpan riwayat treatment dan preferensi setiap pelanggan</p>
          </div>

          <!-- Feature 4 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-pink-100 dark:bg-pink-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-chart-bar" class="w-6 h-6 text-pink-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Laporan Real-time</h3>
            <p class="text-gray-600 dark:text-gray-300">Dashboard analitik untuk monitor performa bisnis Anda</p>
          </div>

          <!-- Feature 5 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-green-100 dark:bg-green-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-banknotes" class="w-6 h-6 text-green-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Manajemen Keuangan</h3>
            <p class="text-gray-600 dark:text-gray-300">Kelola pembayaran, invoice, dan laporan keuangan dengan mudah</p>
          </div>

          <!-- Feature 6 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-blue-100 dark:bg-blue-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-cube" class="w-6 h-6 text-blue-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Inventori Produk</h3>
            <p class="text-gray-600 dark:text-gray-300">Track stok produk dan bahan salon secara otomatis</p>
          </div>

          <!-- Feature 7 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-orange-100 dark:bg-orange-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-bell-alert" class="w-6 h-6 text-orange-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Reminder Otomatis</h3>
            <p class="text-gray-600 dark:text-gray-300">Kirim notifikasi WhatsApp/SMS untuk appointment reminder</p>
          </div>

          <!-- Feature 8 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-teal-100 dark:bg-teal-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-user-group" class="w-6 h-6 text-teal-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Manajemen Staff</h3>
            <p class="text-gray-600 dark:text-gray-300">Kelola jadwal, komisi, dan performa karyawan dengan mudah</p>
          </div>

          <!-- Feature 9 -->
          <div class="bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-800/50 rounded-xl p-6 border border-gray-200 dark:border-gray-700 hover:shadow-lg transition-shadow">
            <div class="w-12 h-12 bg-rose-100 dark:bg-rose-900/30 rounded-lg flex items-center justify-center mb-4">
              <UIcon name="i-heroicons-building-storefront" class="w-6 h-6 text-rose-500" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Multi-Cabang</h3>
            <p class="text-gray-600 dark:text-gray-300">Kelola beberapa cabang salon dari satu dashboard terpusat</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="py-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-r from-primary-500 to-purple-600">
      <div class="max-w-7xl mx-auto">
        <div class="grid md:grid-cols-3 gap-8 text-center text-white">
          <div>
            <div class="text-5xl font-bold mb-2">1000+</div>
            <div class="text-xl opacity-90">Salon Terdaftar</div>
          </div>
          <div>
            <div class="text-5xl font-bold mb-2">50K+</div>
            <div class="text-xl opacity-90">Booking per Bulan</div>
          </div>
          <div>
            <div class="text-5xl font-bold mb-2">98%</div>
            <div class="text-xl opacity-90">Kepuasan Pelanggan</div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">
          Siap Tingkatkan Bisnis Salon Anda?
        </h2>
        <p class="text-xl text-gray-600 dark:text-gray-300 mb-8">
          Bergabunglah dengan ribuan salon yang sudah menggunakan sistem kami
        </p>
        <NuxtLink to="/auth/register">
          <UButton size="xl" class="shadow-lg hover:shadow-xl transition-shadow">
            <UIcon name="i-heroicons-rocket-launch" class="w-5 h-5 mr-2" />
            Mulai Gratis Sekarang
          </UButton>
        </NuxtLink>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <div class="grid md:grid-cols-4 gap-8">
          <div>
            <div class="flex items-center space-x-2 mb-4">
              <UIcon name="i-heroicons-scissors" class="w-6 h-6 text-primary-500" />
              <span class="text-lg font-bold text-white">Salon MS</span>
            </div>
            <p class="text-sm">Solusi manajemen salon terbaik untuk bisnis Anda</p>
          </div>
          <div>
            <h4 class="font-semibold text-white mb-4">Produk</h4>
            <ul class="space-y-2 text-sm">
              <li><a href="#" class="hover:text-primary-400 transition-colors">Fitur</a></li>
              <li><a href="#" class="hover:text-primary-400 transition-colors">Harga</a></li>
              <li><a href="#" class="hover:text-primary-400 transition-colors">Demo</a></li>
            </ul>
          </div>
          <div>
            <h4 class="font-semibold text-white mb-4">Perusahaan</h4>
            <ul class="space-y-2 text-sm">
              <li><a href="#" class="hover:text-primary-400 transition-colors">Tentang Kami</a></li>
              <li><a href="#" class="hover:text-primary-400 transition-colors">Blog</a></li>
              <li><a href="#" class="hover:text-primary-400 transition-colors">Kontak</a></li>
            </ul>
          </div>
          <div>
            <h4 class="font-semibold text-white mb-4">Legal</h4>
            <ul class="space-y-2 text-sm">
              <li><a href="#" class="hover:text-primary-400 transition-colors">Privacy Policy</a></li>
              <li><a href="#" class="hover:text-primary-400 transition-colors">Terms of Service</a></li>
            </ul>
          </div>
        </div>
        <div class="border-t border-gray-800 mt-8 pt-8 text-center text-sm">
          <p>&copy; 2025 Salon Management System. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
// Smooth scroll for anchor links
const handleSmoothScroll = (e: Event) => {
  const target = e.target as HTMLAnchorElement
  if (target.hash) {
    e.preventDefault()
    const element = document.querySelector(target.hash)
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' })
    }
  }
}

onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', handleSmoothScroll)
  })
})
</script>