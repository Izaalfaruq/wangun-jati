<template>
    <div class="space-y-6">
      <div v-for="item in contactInfo" :key="item.title" class="flex items-start gap-4">
        <div class="p-3 bg-blue-50 rounded-lg">
          <i :class="item.icon + ' text-xl text-blue-600'"></i>
        </div>
        <div>
          <h3 class="font-semibold text-lg mb-1">{{ item.title }}</h3>
          <p class="text-gray-600">{{ item.content }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const contactInfo = [
    {
      icon: 'pi pi-map-marker',
      title: 'Alamat',
      content: 'Jl. Kesesi Kaliwadas No.10 RT 04 Rw 03 Kesesi, Pekalongan'
    },
    {
      icon: 'pi pi-envelope',
      title: 'Email',
      content: 'wangunjatikonstruksi1@gmail.com'
    },
    {
      icon: 'pi pi-phone',
      title: 'Phone',
      content: '085867565682'
    },
    
  ];
  </script>