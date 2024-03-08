<template>
    <div class="grid grid-cols-2 lg:grid-cols-5 justify-center items-center gap-10 px-6 md:px-10 lg:px-20 xl:px-28">
      <div class="flex items-center justify-center" v-for="(img , index) in Images" :key="index" :class="{'col-span-2 lg:col-span-1 mx-auto md:mx-0' : index === 4}">
        <img :src="getStaticImagePath(index)" :alt="img.imgAlt">
      </div>
    </div>
  </template>
  
  <script setup>
  import { reactive } from 'vue';
  
  const Images = reactive([
    { imgAlt: 'img1' },
    { imgAlt: 'img2' },
    { imgAlt: 'img3' },
    { imgAlt: 'img4' },
    { imgAlt: 'img5' },
  ]);
  
  const getStaticImagePath = (index) => {
    // Assuming static images are located in a folder named "src/assets"
    const imageNames = ['Bitmap.png', 'Bitmap (1).png', 'Bitmap (2).png', 'Bitmap (3).png', 'Bitmap (4).png'];
    return `src/assets/${imageNames[index]}`;
  };
  </script>
  
  <style scoped>
  /* Add your custom styles here */
  </style>
  