<template>
  <nav class="bg-gray-900 py-4 flex justify-between items-center px-4 lg:px-14 xl:px-16">
    <router-link to="/">
      <img src="../assets/logo (1).png" alt="">
    </router-link>
    <div>
      <div v-if="!isMenuOpen" class="hidden md:flex space-x-10 lg:space-x-14 xl:space-x-16 2xl:space-x-40 text-white">
        <router-link
          v-for="(item, index) in navbarItems"
          :key="index"
          :to="item.path"
          class="hover:bg-white hover:scale-110 hover:shadow-2xl hover:text-black text-xl px-4 py-2 rounded transition-all ease-in-out duration-500 delay-75"
        >
          {{ item.label }}
        </router-link>
      </div>
    </div>
    <div class="hidden md:block">
      <button
        class="text-white px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out hover:border-white hover:scale-110 duration-500 hover:bg-gray-600"
      >
        Contact
      </button>
    </div>
    <button class="text-white text-xl md:hidden" @click="toggleMenu">
      <template v-if="isMenuOpen">
        <!-- SVG for close icon -->
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
        </svg>
      </template>
      <template v-else>
        <!-- SVG for open icon -->
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      </template>
    </button>
  </nav>
  <div 
    :class="{ 'scale-y-100 h-1 border-t border-gray-700': isMenuOpen, 'scale-y-0 h-0': !isMenuOpen }"
    class="transform transition-all duration-500 ease-in-out origin-top block md:hidden"
  >
    <ul class="p-4 space-y-4 bg-gray-900 bg-opacity-95">
      <li
        v-for="(item, index) in navbarItems"
        :key="index"
      >
        <router-link :to="item.path" class="text-white hover:text-blue-200">{{ item.label }}</router-link>
      </li>
      <!-- Add more menu items here -->
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const navbarItems = [
  { path: '/', label: 'About' },
  { path: '/', label: 'Services' },
  { path: '/', label: 'Pricing' },
  { path: '/', label: 'Blog' },
];
</script>

<style scoped>

</style>
