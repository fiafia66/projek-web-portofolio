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

      <!-- SECTION: KEAHLIAN / TECH STACK -->
      <section id="skills" class="w-full max-w-7xl mx-auto px-8 sm:px-12 pt-16 py-16 text-center">
        
        <!-- JUDUL SECTION -->
        <h2 class="text-3xl font-extrabold text-[#432818] mb-4">Bahasa & Tools yang Dipelajari</h2>

        <!-- DESKRIPSI RINGKAS -->
        <p class="max-w-2xl mx-auto text-[#432818]/80 text-base leading-relaxed mb-10">
          Sebagai siswa Rekayasa Perangkat Lunak, saat ini saya sedang menikmati proses eksplorasi dan mempelajari berbagai dasar pengembangan perangkat lunak. 
          Berikut adalah beberapa bahasa dan tools yang sedang saya pelajari:
        </p>

        <!-- GRID IKON TECH STACK -->
        <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-6 gap-6 items-center justify-center">
          
          <!-- HTML5 -->
          <div class="flex flex-col items-center justify-center p-4 bg-[#c29b62] rounded-xl transition-all duration-300 shadow-md">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" class="w-12 h-12 mb-2" />
            <span class="text-sm font-semibold text-[#432818]">HTML5</span>
          </div>

          <!-- CSS3 -->
          <div class="flex flex-col items-center justify-center p-4 bg-[#c29b62] rounded-xl transition-all duration-300 shadow-md">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3" class="w-12 h-12 mb-2" />
            <span class="text-sm font-semibold text-[#432818]">CSS3</span>
          </div>

          <!-- PHP -->
          <div class="flex flex-col items-center justify-center p-4 bg-[#c29b62] rounded-xl transition-all duration-300 shadow-md">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="PHP" class="w-12 h-12 mb-2" />
            <span class="text-sm font-semibold text-[#432818]">PHP</span>
          </div>

          <!-- MySQL -->
          <div class="flex flex-col items-center justify-center p-4 bg-[#c29b62] rounded-xl transition-all duration-300 shadow-md">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL" class="w-12 h-12 mb-2" />
            <span class="text-sm font-semibold text-[#432818]">MySQL</span>
          </div>

          <!-- Java -->
          <div class="flex flex-col items-center justify-center p-4 bg-[#c29b62] rounded-xl transition-all duration-300 shadow-md">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java" class="w-12 h-12 mb-2" />
            <span class="text-sm font-semibold text-[#432818]">Java</span>
          </div>

          <!-- Figma -->
          <div class="flex flex-col items-center justify-center p-4 bg-[#c29b62] rounded-xl transition-all duration-300 shadow-md">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" alt="Figma" class="w-12 h-12 mb-2" />
            <span class="text-sm font-semibold text-[#432818]">Figma</span>
          </div>

        </div>
      </section>

      <!-- SECTION: YANG DAPAT SAYA LAKUKAN -->
      <section id="services" class="w-full max-w-7xl mx-auto px-8 sm:px-12 py-8 text-center">
        
        <!-- JUDUL SECTION -->
        <h2 class="text-3xl font-extrabold text-[#432818] mb-4">Yang Dapat Saya Lakukan</h2>

        <!-- DESKRIPSI RINGKAS -->
        <p class="max-w-2xl mx-auto text-[#432818]/80 text-base leading-relaxed mb-12">
          Berbekal materi pelajaran di SMK dan beberapa proyek latihan, berikut adalah hal-hal yang sedang saya pelajari dan kembangkan:
        </p>

        <!-- GRID CARD 3 KOLOM -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          
          <!-- CARD 1: Logika & Pemrograman -->
          <div class="p-8 bg-[#c29b62] rounded-2xl shadow-md hover:shadow-lg transition-all duration-300 text-center flex flex-col items-center">
            <div class="w-14 h-14 mb-6 text-[#432818]">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-full h-full">
                <path stroke-linecap="round" stroke-linejoin="round" d="M20.25 6.375c0 2.278-3.694 4.125-8.25 4.125S3.75 8.653 3.75 6.375m16.5 0c0-2.278-3.694-4.125-8.25-4.125S3.75 4.097 3.75 6.375m16.5 0v11.25c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125V6.375m16.5 5.625c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-[#432818] mb-3">Logika & Pemrograman</h3>
            <p class="text-sm text-[#432818]/80 leading-relaxed">
              Memahami alur logika pemrograman dan terus memperdalam.
            </p>
          </div>

          <!-- CARD 2: Tampilan Website Sederhana -->
          <div class="p-8 bg-[#c29b62] rounded-2xl shadow-md hover:shadow-lg transition-all duration-300 text-center flex flex-col items-center">
            <div class="w-14 h-14 mb-6 text-[#432818]">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-full h-full">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9 9 0 100-18 9 9 0 000 18zm0 0a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-[#432818] mb-3">Tampilan Website Sederhana</h3>
            <p class="text-sm text-[#432818]/80 leading-relaxed">
              Belajar menyusun dan mengoreksi tampilan web statis seperti landing page atau portofolio menggunakan HTML dan CSS agar responsif.
            </p>
          </div>

          <!-- CARD 3: Eksplorasi Desain UI -->
          <div class="p-8 bg-[#c29b62] rounded-2xl shadow-md hover:shadow-lg transition-all duration-300 text-center flex flex-col items-center">
            <div class="w-14 h-14 mb-6 text-[#432818]">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-full h-full">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9.53 16.122a3 3 0 00-5.78 1.128 2.25 2.25 0 01-2.4 2.245 4.5 4.5 0 008.4-2.245c0-.388-.073-.761-.22-1.128zm0 0a15.998 15.998 0 003.388-1.62m-5.006 0a15.998 15.998 0 011.618-3.388m0 0a15.998 15.998 0 003.388 1.62m-1.62-3.388a15.998 15.998 0 01-3.388-1.618m0 0a15.998 15.998 0 00-1.62 3.388" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-[#432818] mb-3">Eksplorasi Desain UI</h3>
            <p class="text-sm text-[#432818]/80 leading-relaxed">
              Mencoba merancang tata letak dan prototipe tampilan antarmuka web sederhana menggunakan Figma sebelum dipindahkan ke kode.
            </p>
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