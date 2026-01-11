<template>
  <main>
    <PageHeader title="Tentang Kami" />

    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
          <div>
            <!-- <h2 class="text-3xl font-bold mb-6">Our Story</h2> -->
            <p class="text-gray-600 mb-4">
              Kami adalah perusahaan konstruksi jalan yang berfokus pada
              pekerjaan pengaspalan berkualitas tinggi untuk mendukung
              kelancaran mobilitas dan aktivitas ekonomi. Dengan tenaga ahli
              berpengalaman serta peralatan modern, kami memastikan setiap
              proyek dikerjakan secara presisi, efisien, dan sesuai standar
              teknis yang berlaku.
            </p>
            <p class="text-gray-600 mb-6">
              Kami berkomitmen menghadirkan permukaan jalan yang kuat, aman, dan
              tahan lama melalui pemilihan material yang tepat serta pengelolaan
              proyek yang sistematis. Fokus kami tidak hanya pada penyelesaian
              pekerjaan, tetapi juga pada keberlanjutan dan kepuasan klien
              sebagai dasar kemitraan jangka panjang.
            </p>
            <div class="grid grid-cols-2 gap-8">
              <div v-for="stat in stats" :key="stat.label" class="text-center">
                <div class="text-4xl font-bold text-blue-600 mb-2">
                  {{ stat.value }}
                </div>
                <div class="text-gray-600">{{ stat.label }}</div>
              </div>
            </div>
          </div>
          <!-- <div class="relative">
            <img
              src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&q=80&w=800"
              alt="Team meeting"
              class="rounded-lg shadow-xl"
            />
          </div> -->
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
import PageHeader from "@/components/shared/PageHeader.vue";

// const stats = [
//   { value: "100+", label: "Projects Completed" },
//   { value: "50+", label: "Happy Clients" },
//   { value: "15+", label: "Team Members" },
//   { value: "4+", label: "Years Experience" },
// ];
</script>
