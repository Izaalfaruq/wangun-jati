<template>
  <footer class="bg-gray-900 text-white py-12">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mx-auto">
        <div>
          <div class="flex items-center gap-2 mb-4">
            <h3 class="font-bold text-xl" style="color: #ebed9e">Wangun Jati</h3>
          </div>
          <p class="text-gray-400">
            Crafting digital experiences that inspire and innovate.
          </p>
        </div>
        <div>
          <h3 class="font-bold mb-4" style="color: #ebed9e">Layanan</h3>
          <ul class="space-y-2 text-gray-400">
            <li>
              <router-link
                to="/services"
                class="hover:text-blue-400 transition-colors"
                >Pengaspalan Jalan Baru</router-link
              >
            </li>
            <li>
              <router-link
                to="/services"
                class="hover:text-blue-400 transition-colors"
                >Perbaikan & Pemeliharaan Jalan</router-link
              >
            </li>
            <li>
              <router-link
                to="/services"
                class="hover:text-blue-400 transition-colors"
                >Pelapisan Ulang Jalan (Overlay)</router-link
              >
            </li>
          </ul>
        </div>
        <div>
          <h3 class="font-bold mb-4" style="color: #ebed9e">Perusahaan</h3>
          <ul class="space-y-2 text-gray-400">
            <li>
              <router-link
                to="/about"
                class="hover:text-blue-400 transition-colors"
                >Tentang Kami</router-link
              >
            </li>
            <li>
              <router-link
                to="/portfolio"
                class="hover:text-blue-400 transition-colors"
                >Portfolio</router-link
              >
            </li>
            <li>
              <router-link
                to="/contact"
                class="hover:text-blue-400 transition-colors"
                >Kontak</router-link
              >
            </li>
          </ul>
        </div>
      </div>
      <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
        <p>
          &copy; {{ new Date().getFullYear() }} Wangun Jati Konstruksi. All rights
          reserved.
        </p>
      </div>
    </div>
  </footer>
</template>
