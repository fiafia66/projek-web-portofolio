<template>
  <div class="min-h-screen bg-[#faf6f0] text-[#432818] font-sans flex flex-col justify-between">
    
    <!-- NAVBAR FULL WIDTH & STICKY -->
    <header class="sticky top-0 z-50 bg-[#ede0d4]/90 backdrop-blur-md border-b-2 border-[#6f4e37] w-full">
      <div class="w-full px-8 sm:px-12 py-7 flex items-center justify-between">
            
        <!-- Logo -->
        <NuxtLink to="/" class="text-2xl font-extrabold tracking-tight text-[#6f4e37]">
          Portofolio Alifia<span class="text-[#6f4e37]">!</span>
        </NuxtLink>

        <!-- Navigation Menu -->
        <nav class="hidden sm:flex items-center space-x-8 text-lg font-semibold text-[#7f5539]">
          <NuxtLink to="/about" class="hover:text-[#432818] transition-colors">Tentang</NuxtLink>
          <NuxtLink to="/skills" class="hover:text-[#432818] transition-colors">Keahlian</NuxtLink>
          <NuxtLink to="/projects" class="hover:text-[#432818] transition-colors">Karya</NuxtLink>
          
          <!-- Tombol Hubungi Saya di Navbar -->
          <button 
            @click="isContactOpen = true"
            class="inline-block px-3.5 py-1.5 text-[15px] font-semibold bg-[#ddb892] border border-[#7f5539] rounded-none text-[#432818] hover:bg-[#b08968] transition-all text-center cursor-pointer"
          >
            Hubungi Saya
          </button>
        </nav>
      </div>
    </header>

    <!-- OVERLAY (BACKGROUND GELAP) -->
    <div 
      v-if="isContactOpen" 
      @click="isContactOpen = false"
      class="fixed inset-0 bg-black/50 z-50 transition-opacity"
    ></div>

    <!-- PANEL SLIDE-OVER GET IN TOUCH (MUNCUL DARI SAMPING KANAN) -->
    <div 
      class="fixed top-0 right-0 h-full w-full max-w-sm bg-[#fdf0d5] text-gray-800 z-50 shadow-2xl p-6 transform transition-transform duration-300 ease-in-out flex flex-col justify-between"
      :class="isContactOpen ? 'translate-x-0' : 'translate-x-full'"
    >
      <div>
        <!-- Header Panel & Tombol Close (X) -->
        <div class="flex justify-between items-center mb-8 border-b border-[#7f5539]/20 pb-4">
          <h2 class="text-2xl font-bold text-[#432818]">Get in Touch</h2>
          <button 
            @click="isContactOpen = false" 
            class="text-gray-500 hover:text-black font-bold text-2xl w-8 h-8 flex items-center justify-center rounded-full hover:bg-black/5 transition cursor-pointer"
          >
            &times;
          </button>
        </div>

        <!-- Detail Informasi Kontak -->
        <div class="space-y-5 text-sm">
          <div class="flex items-center gap-4">
            <span class="text-xl">📧</span>
            <div>
              <p class="text-xs text-gray-500 font-medium">Email</p>
              <p class="font-semibold text-gray-800">alifjuni1506@gmail.com</p>
            </div>
          </div>

          <div class="flex items-center gap-4">
            <span class="text-xl">📞</span>
            <div>
              <p class="text-xs text-gray-500 font-medium">Telepon / WhatsApp</p>
              <p class="font-semibold text-gray-800">+62 8xx-xxxx-xxxx</p>
            </div>
          </div>

          <div class="flex items-center gap-4">
            <span class="text-xl">📍</span>
            <div>
              <p class="text-xs text-gray-500 font-medium">Lokasi</p>
              <p class="font-semibold text-gray-800">Jakarta, Indonesia</p>
            </div>
          </div>
        </div>

        <hr class="my-6 border-gray-300" />

        <!-- Sosial Media -->
        <div>
          <p class="text-sm font-semibold text-gray-600 mb-3">Social Media</p>
          <div class="flex gap-3 text-lg">
            <a href="https://github.com/fiafia66" target="_blank" class="p-2.5 bg-white rounded-full hover:bg-gray-100 shadow-sm transition">🐙</a>
            <a href="mailto:alifjuni1506@gmail.com" class="p-2.5 bg-white rounded-full hover:bg-gray-100 shadow-sm transition">📧</a>
          </div>
        </div>
      </div>

      <!-- Footer Kecil di dalam Panel -->
      <div class="text-xs text-center text-gray-400 pt-4 border-t border-gray-300">
        Portofolio RPL • 2026
      </div>
    </div>

    <!-- MAIN KONTEN -->
    <main class="space-y-16 pb-20">

      <!-- SECTION: PROYEK SAYA -->
      <section id="projects" class="w-full max-w-7xl mx-auto pt-16 px-8 sm:px-12 py-16 text-center">
        
        <!-- JUDUL SECTION -->
        <h2 class="text-3xl font-extrabold text-[#432818] mb-4">Proyek Saya</h2>

        <!-- DESKRIPSI RINGKAS -->
        <p class="max-w-2xl mx-auto text-[#432818]/80 text-base leading-relaxed mb-12">
          Berikut adalah beberapa proyek dan tugas yang pernah saya kerjakan sejauh ini di SMK:
        </p>

        <!-- GRID CARD PROYEK (3 KOLOM) -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          
          <!-- CARD PROYEK 1: WEB RESTO -->
          <div class="bg-[#c29b62] rounded-2xl border overflow-hidden shadow-md flex flex-col text-left">
            <div class="w-full h-48 bg-[#e7d8c9]/60 flex items-center justify-center overflow-hidden">
              <img src="/resto.png" alt="Proyek Web Resto" class="w-full h-full object-cover" />
            </div>
            <div class="p-6 flex flex-col flex-grow justify-between">
              <div>
                <h3 class="text-xl font-bold text-[#432818] mb-2">Website Restoran</h3>
                <p class="text-sm text-[#432818] leading-relaxed mb-4">
                  Website restoran interaktif dengan fitur multi halaman yang mencakup katalog menu, profil, dan sistem halaman login.
                </p>
              </div>
              <div>
                <div class="flex flex-wrap gap-2 mb-6">
                  <span class="px-3 py-1 bg-[#432818] text-[#e7d8c9] text-xs font-semibold rounded-full">HTML</span>
                  <span class="px-3 py-1 bg-[#432818] text-[#e7d8c9] text-xs font-semibold rounded-full">CSS</span>
                </div>
                <a href="https://fiafia66.github.io/projek-web-resto/" target="_blank" class="inline-block w-full text-center py-2 px-4 bg-[#432818] text-[#e7d8c9] font-medium text-sm rounded-xl hover:bg-[#432818]/90 transition-all duration-300">
                  Lihat Proyek
                </a>
              </div>
            </div>
          </div>

          <!-- CARD PROYEK 2: UI/UX MOBILE APP -->
          <div class="bg-[#c29b62] rounded-2xl border overflow-hidden shadow-md flex flex-col text-left">
            <div class="w-full h-48 bg-[#e7d8c9]/60 flex items-center justify-center overflow-hidden">
              <img src="/roti.png" alt="Proyek 2" class="w-full h-full object-cover" />
            </div>
            <div class="p-6 flex flex-col flex-grow justify-between">
              <div>
                <h3 class="text-xl font-bold text-[#432818] mb-2">UI/UX Mobile App Design</h3>
                <p class="text-sm text-[#432818] leading-relaxed mb-4">
                  Desain antarmuka dan prototype aplikasi seluler interaktif untuk platform digital, lengkap dengan alur navigasi pengguna (user flow) dari halaman utama hingga autentikasi.
                </p>
              </div>
              <div>
                <div class="flex flex-wrap gap-2 mb-6">
                  <span class="px-3 py-1 bg-[#432818] text-[#e7d8c9] text-xs font-semibold rounded-full">Figma</span>
                </div>
                <a href="https://www.figma.com/proto/zp7K086ZQfrZZSu3CUfp9H/Untitled?node-id=53-107&p=f&m=draw&scaling=scale-down&content-scaling=fixed&page-id=53%3A77&t=DR5LVCdqvFx1bq3U-1" target="_blank" class="inline-block w-full text-center py-2 px-4 bg-[#432818] text-[#e7d8c9] font-medium text-sm rounded-xl hover:bg-[#432818]/90 transition-all duration-300">
                  Lihat Proyek
                </a>
              </div>
            </div>
          </div>

          <!-- CARD PROYEK 3 -->
          <div class="bg-[#c29b62] rounded-2xl border overflow-hidden shadow-md flex flex-col text-left">
            <div class="w-full h-48 bg-[#e7d8c9]/60 flex items-center justify-center overflow-hidden">
              <img src="https://via.placeholder.com/400x250" alt="Proyek 3" class="w-full h-full object-cover" />
            </div>
            <div class="p-6 flex flex-col flex-grow justify-between">
              <div>
                <h3 class="text-xl font-bold text-[#432818] mb-2">Desain UI Web Sederhana</h3>
                <p class="text-sm text-[#432818] leading-relaxed mb-4">
                  Rancangan tampilan antarmuka (prototype) aplikasi web sederhana yang dibuat menggunakan Figma.
                </p>
              </div>
              <div>
                <div class="flex flex-wrap gap-2 mb-6">
                  <span class="px-3 py-1 bg-[#432818] text-[#e7d8c9] text-xs font-semibold rounded-full">Figma</span>
                  <span class="px-3 py-1 bg-[#432818] text-[#e7d8c9] text-xs font-semibold rounded-full">UI Design</span>
                </div>
                <a href="#" class="inline-block w-full text-center py-2 px-4 bg-[#432818] text-[#e7d8c9] font-medium text-sm rounded-xl hover:bg-[#432818]/90 transition-all duration-300">
                  Lihat Proyek
                </a>
              </div>
            </div>
          </div>

        </div>
      </section>

    </main>

    <!-- FOOTER -->
    <footer class="w-full bg-[#606c38] pt-12 pb-8">
      <div class="max-w-7xl mx-auto px-8 sm:px-12">
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 pb-8">
          
          <!-- Kolom 1 -->
          <div class="space-y-2">
            <h3 class="text-xl font-extrabold text-[#ffffff]">Alifia Junianty</h3>
            <p class="text-sm text-[#ffffff] max-w-xs leading-relaxed">
              Aktif belajar, berkarya, dan terus mengeksplorasi berbagai hal baru di bidang pemrograman serta pengembangan perangkat lunak.
            </p>
          </div>

          <!-- Kolom 2 -->
          <div class="space-y-2">
            <h4 class="text-lg font-bold text-[#ffffff]">Tautan Cepat</h4>
            <ul class="space-y-1.5 text-sm font-medium text-[#ffffff]">
              <li><NuxtLink to="/about" class="hover:underline transition-colors">Tentang</NuxtLink></li>
              <li><NuxtLink to="/skills" class="hover:underline transition-colors">Keahlian</NuxtLink></li>
              <li><NuxtLink to="/projects" class="hover:underline transition-colors">Karya</NuxtLink></li>
              <li><button @click="isContactOpen = true" class="hover:underline transition-colors text-left cursor-pointer">Hubungi Saya</button></li>
            </ul>
          </div>

          <!-- Kolom 3 -->
          <div class="space-y-2">
            <h4 class="text-lg font-bold text-[#ffffff]">Connect</h4>
            <div class="flex items-center gap-4 pt-1">
              <!-- Email -->
              <a href="mailto:alifjuni1506@gmail.com" class="p-2.5 bg-white rounded-lg text-[#432818] hover:bg-[#faf6f0] transition shadow-sm flex items-center justify-center" title="Email">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 fill-current" viewBox="0 0 24 24">
                  <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
                </svg>
              </a>
              <!-- Github -->
              <a href="https://github.com/fiafia66" target="_blank" rel="noopener noreferrer" class="p-2.5 bg-white rounded-lg text-[#432818] hover:bg-[#faf6f0] transition shadow-sm flex items-center justify-center" title="GitHub">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 fill-current" viewBox="0 0 24 24">
                  <path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/>
                </svg>
              </a>
            </div>
          </div>

        </div>

        <div class="pt-6 text-center text-xs text-[#ffffff] border-t border-white/20">
          <p>© 2026 Alifia Junianty. Hak cipta dilindungi.</p>
        </div>

      </div>
    </footer>

  </div>
</template>

<script setup>
import { ref } from 'vue'

// State untuk mengatur buka/tutup slide-over Get in Touch
const isContactOpen = ref(false)
</script>