<template>
  <main>
    <!-- Hero Section -->
    <section
      id="home"
      class="min-h-screen flex items-center relative overflow-hidden"
    >
      <div
        class="container mx-auto px-4 grid grid-cols-1 md:grid-cols-2 gap-12 items-center mt-8 pt-8 md:mt-0 md:pt-4"
      >
        <!-- Left Content -->
        <div class="text-left">
          <h1
            class="text-5xl md:text-5xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-blue-600 to-purple-600"
            style="line-height: 1.25 !important"
          >
            Solusi

            <span class="relative">
              <span
                class="bg-clip-text text-transparent bg-gradient-to-r from-blue-600 to-purple-600"
              >
                Infrasturktur
              </span>
              <span
                class="absolute left-0 -bottom-2 w-full h-2 bg-[#f9ff00] rounded-md"
              ></span>
            </span>
            Jalan
          </h1>
          <p class="text-xl text-gray-600 mb-8">
            Kami menghadirkan solusi infrastruktur jalan yang terukur dan
            berstandar tinggi. Setiap proyek dijalankan dengan manajemen
            profesional untuk memastikan kualitas dan keandalan jangka panjang.
          </p>
          <!-- <div class="flex gap-4">
            <Button
              @click="navigateToSection('services')"
              label="Get Started"
              icon="pi pi-arrow-right"
              class="p-button-rounded p-button-lg custom-get-started"
            />
            <Button
              @click="navigateToSection('portfolio')"
              label="Our Work"
              icon="pi pi-images"
              class="p-button-rounded p-button-lg custom-our-work"
            />
          </div> -->
        </div>
        <!-- Right Illustration -->
        <div class="relative">
          <img
            src="/logo.png"
            alt="Creative workspace"
            class="rounded-2xl transform hover:scale-105 transition-transform duration-300"
          />
          <!-- Decorative Elements -->
          <div
            class="absolute -top-8 -right-8 w-32 h-32 bg-blue-500/10 rounded-full blur-2xl"
          ></div>
          <div
            class="absolute -bottom-8 -left-8 w-32 h-32 bg-purple-500/10 rounded-full blur-2xl"
          ></div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-20 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">Layanan Kami</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <ServiceCard
            v-for="service in services.slice(0, 3)"
            :key="service.title"
            v-bind="service"
          />
        </div>
        <!-- <div class="text-center mt-12">
          <router-link to="/services">
            <Button
              label="Lihat Semua Layanan"
              severity="secondary"
              class="p-button-rounded"
            />
          </router-link>
        </div> -->
      </div>
    </section>

    <!-- Portfolio Preview -->
    <section id="portfolio" class="py-20 bg-gray-50">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">Proyek</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <ProjectCard
            v-for="project in projects.slice(0, 3)"
            :key="project.title"
            v-bind="project"
          />
        </div>
        <!-- <div class="text-center mt-12">
          <router-link to="/portfolio">
            <Button
              label="Lihat Semua Proyek"
              icon="pi pi-arrow-right"
              severity="secondary"
              class="p-button-rounded"
            />
          </router-link>
        </div> -->
      </div>
    </section>

    <!-- About Preview -->
    <section id="about" class="py-20 bg-white">
      <div
        class="container mx-auto px-4 grid grid-cols-1 md:grid-cols-2 gap-12 items-center"
      >
        <div>
          <h2 class="text-3xl font-bold mb-6">Siapa Kami?</h2>
          <p class="text-gray-600 mb-8">
            Kami adalah perusahaan konstruksi yang berfokus pada pengembangan
            dan peningkatan infrastruktur jalan secara profesional dan
            berstandar tinggi. Dengan keahlian teknis yang kuat, manajemen
            proyek yang terstruktur, serta komitmen terhadap kualitas, kami
            menghadirkan solusi rekayasa jalan yang aman, efisien, dan
            berkelanjutan untuk mendukung pertumbuhan dan konektivitas berbagai
            sektor.
          </p>
          <router-link to="/about">
            <Button
              label="Lihat Lebih Lanjut"
              icon="pi pi-arrow-right"
              severity="secondary"
              class="p-button-rounded"
            />
          </router-link>
        </div>
        <div class="relative">
          <img
            src="/logo.png"
            alt="Our team"
            class="rounded-2xl transform hover:scale-105 transition-transform duration-300"
          />
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section
      id="contact"
      class="py-20 bg-gradient-to-r from-blue-600 to-purple-600 text-white"
    >
      <div class="container mx-auto px-4 text-center">
        <h2 class="text-4xl font-bold mb-6">Jika Anda Membutuhkan Jasa Kami</h2>
        <router-link to="/contact">
          <Button
            label="Kontak Kami"
            icon="pi pi-send"
            class="p-button-rounded p-button-lg p-button-outlined"
          />
        </router-link>
      </div>
    </section>
  </main>
</template>

<script setup>
import ServiceCard from "@/components/services/ServiceCard.vue";
import ProjectCard from "@/components/portfolio/ProjectCard.vue";
import { services } from "@/data/services";
import { projects } from "@/data/projects";

const navigateToSection = (id) => {
  const element = document.getElementById(id);
  if (element) {
    element.scrollIntoView({ behavior: "smooth" });
  }
};
</script>

<style scoped>
/* Custom "Get Started" Button */
.custom-get-started {
  background-color: #ebed9e !important;
  color: #000 !important;
  border: none !important;
  width: 140px;
  height: 40px;
  padding: 8px 10px;
}

.custom-get-started:hover {
  background-color: #f2ff00 !important; /* Slightly darker shade for hover */
}

/* Custom "Our Work" Button */
.custom-our-work {
  background-color: #5a58e9 !important;
  color: #fff !important;
  border: none !important;
  width: 140px;
  height: 40px;
  padding: 8px 15px;
}

.custom-our-work:hover {
  background-color: #4745c9 !important; /* Slightly darker shade for hover */
}
</style>
