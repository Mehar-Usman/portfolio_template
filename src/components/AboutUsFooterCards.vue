<template>
    <div class="grid grid-cols-1 md:grid-cols-3 px-6 md:px-10 lg:px-20 py-20 xl:px-28 gap-10 md:gap-0">
      <div v-for="(card, index) in cards" :key="index">
        <article>
          <div :class="[
            'p-6 border border-gray-900 rounded hover:bg-gray-900 group transition-all ease-in-out duration-500 ',
            { 'border md:border-t md:border-b md:border-l-0 md:border-r-0': index === 1 },
            { 'rounded  md:rounded-none md:rounded-l': index === 0 },
            { 'rounded md:rounded-none': index === 1 },
            { 'rounded md:rounded-none md:rounded-r': index === 2 },
          ]">
            <h1 class=" group-hover:text-white group-hover:translate-x-5 transition-all duration-500 ease-in-out">{{ card.title }}</h1>
            <p class="mt-3 group-hover:text-white group-hover:translate-x-5 transition-all duration-500 ease-in-out ">{{ card.content }}</p>
          </div>
        </article>
      </div>
    </div>
  </template>
  
  <script setup>
    import { reactive } from 'vue';
    const cards = reactive([
      { title: '42%', content: 'Years of experience' },
      { title: '73+', content: 'Agency members' },
      { title: '5.000', content: 'Projects complete' }
    ]);
  </script>
  
  <style>
    /* Add your custom styles here */
  </style>
  