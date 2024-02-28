<template>
  <div class="bg-gray-900 px-6 md:px-10 lg:px-20  xl:px-28 py-10">
    <header class=" pb-10">
      <p class="text-2xl text-orange-500 mt-3 uppercase">our team</p>
      <h1 class="text-white text-2xl md:text-4xl lg:text-5xl w-full md:w-3/5 font-900 mt-3">Team of Designers and Developers</h1>
    </header>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
      <article class="border rounded"  v-for="(card , index) in cards" :key="index">
        <figure class="border border-gray-700 shadow-2xl rounded h-[270px] flex items-end justify-center pt-5">
          <img :src="card.imgSrc" alt="">
        </figure>
        <div class="py-4 text-center">
          <h3 class="text-white">{{ card.name }}</h3>
          <p class="text-gray-500">{{ card.userRole }}</p>
        </div>

      </article>
    </div>
  </div>
</template>
<script setup>
    import {reactive} from 'vue';
    const cards = reactive([
      {imgSrc:'src/assets/employe-1.png', name:'Azah Anyeni', userRole:'Designer'},
      {imgSrc:'src/assets/employe-2.png', name:'Roelof Bekkenenks', userRole:'React developer'},
      {imgSrc:'src/assets/employe-3.png', name:'Leonardo Oliveira', userRole:'Vue js Developer'},
      {imgSrc:'src/assets/employe-4.png', name:'Izabella Tabakova', userRole:'Php Developer'}
    ])
</script>
<style>
  
</style>