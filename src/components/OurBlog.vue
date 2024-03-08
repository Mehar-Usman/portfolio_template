<template>
  <div class="bg-orange-100 px-6 md:px-10 lg:px-20 py-12 xl:px-28">
    <div>
      <p class="text-2xl uppercase text-orange-500">Our Blog</p>
      <div class="flex justify-between items-center mt-6">
        <div>
          <p class="text-5xl font-bold">Latest Blog Articles</p>
        </div>
        <div>
          <button class="text-black bg-white shadow-2xl uppercase px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">
            Discover All
          </button>
        </div>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-10">
        <article class="blog-card bg-white hover:bg-gray-900 transition-all ease-in-out duration-500 group" v-for="(blogCard, index) in blogCards" :key="index">
          <img :src="getStaticImagePath(index)" alt="Blog Image" class="w-full h-40 object-cover">
          <div class="p-4">
            <p class="text-sm text-gray-500 group-hover:text-white transition-all ease-in-out duration-500">{{ blogCard.blogDate }}</p>
            <h3 class="text-xl font-semibold text-gray-800 mt-2 group-hover:text-white transition-all ease-in-out duration-500">{{ blogCard.blogTitle }}</h3>
            <p class="text-gray-600 mt-2 group-hover:text-white transition-all ease-in-out duration-500">{{ blogCard.blogDescription }}</p>
          </div>
        </article>
      </div>
      <div class="mt-16">
        <hr class="w-full h-[2px] bg-orange-200">
      </div>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const blogCards = reactive([
  { blogTitle: 'Stories', blogDescription: 'Agency is a business you hire to outsource', blogDate: '5 Nov, 2021' },
  { blogTitle: 'Design', blogDescription: 'Outsource your digital marketing efforts', blogDate: '29 Oct, 2021' },
  { blogTitle: 'Marketing', blogDescription: 'Your business with a variety of digital', blogDate: '21 Oct, 2021' },
]);

const getStaticImagePath = (index) => {
  // Assuming static images are located in a folder named "assets"
  const imageNames = ['our-blog1.png', 'our-blog2.png', 'our-blog3.png'];
  return `/src/assets/${imageNames[index]}`;
};
</script>

<style scoped>
.blog-card {
  border-radius: 1rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: all 0.3s ease;
}

.blog-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.15);
}
</style>
