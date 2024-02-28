<template>
    <div class="bg-orange-100 px-6 md:px-10 lg:px-20 xl:px-28 py-20">
    <div>
        <p class="uppercase text-orange-500 text-2xl">service</p>
        <h1 class="text-[29px] md:text-4xl mt-4 font-900  w-full xl:w-1/3 ">How Our Agency  Can Help</h1>
    </div>
    <div class="bg-orange-100 grid grid-cols-1 md:grid-cols-3 py-10 gap-10 md:gap-0 ">
      <div v-for="(card, index) in cards" :key="index">
        <article>
          <div :class="[
            'p-8 border border-gray-900 rounded shadow-2xl hover:bg-gray-900 group transition-all ease-in-out duration-500  h-[350px] lg:h-[330px] xl:h-[320px]',
            { 'border md:border-t md:border-b md:border-l-0 md:border-r-0': index === 1 },
            { 'rounded  md:rounded-none md:rounded-l': index === 0 },
            { 'rounded md:rounded-none': index === 1 },
            { 'rounded md:rounded-none md:rounded-r': index === 2 },
          ]">
            <header class="bg-orange-500 w-14 h-14 rounded-full flex items-center justify-center group-hover:translate-x-5 transition-all duration-500 ease-in-out group-hover:shadow-2xl group-hover:bg-stone-500">
              <img :src="card.imgSrc" alt="">
            </header>
            <section class="mt-4">
                <h1 class=" group-hover:text-white group-hover:translate-x-5 transition-all duration-500 ease-in-out">{{ card.title }}</h1>
                <p class="mt-3 group-hover:text-white group-hover:translate-x-5 transition-all duration-500 ease-in-out ">{{ card.content }}</p>
            </section>
            <footer class="mt-4">
                <button class="bg-gray-900  text-white p-2 rounded-lg uppercase  text-sm tracking-wider group-hover:bg-white group-hover:text-black transition-all duration-500 ease-in-out group-hover:translate-x-5">{{ card.btnText }}</button>
            </footer>
          </div>
        </article>
      </div>
    </div>
</div>

  </template>
  
  <script setup>
    import { reactive } from 'vue';
    const cards = reactive([
      {imgSrc:'src/assets/service-icon-1.png',title:'Design', content:'Agency provides a full service range including technical skills, design.',btnText:'Learn More'},
      {imgSrc:'src/assets/service-icon-2.png',title:'Design', content:'Full service range including technical skills, design, business.',btnText:'Discover More'},
      {imgSrc:'src/assets/service-icon-3.png',title:'Design', content:'Technical skills, design, business understanding, ability.',btnText:'Explore Now'},
    ]);
  </script>
  
  <style>
    /* Add your custom styles here */
  </style>
  