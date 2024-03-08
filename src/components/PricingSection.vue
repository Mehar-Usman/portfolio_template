<template>
  <div class="bg-orange-100 px-6 md:px-10 lg:px-20 py-20 xl:px-28">
    <p class="text-orange-500 text-2xl">Pricing</p>
    <h1 class="text-5xl w-5/6 font-900">Check Our Pricing Plans</h1>
    <div class="grid grid-cols-1 md:grid-cols-3 py-10 items-end gap-10 md:gap-0">
      <div v-for="(card, index) in cards" :key="index" class="">
        <article :class="cardClasses(index)">
          <header :class="headerClasses(index)">
            <div class="bg-orange-500 inline-block px-4 py-2 rounded-2xl mb-5" :class="{ 'hidden': index % 2 === 0 }">
              <p class="text-white text-2xl font-light">Popular</p>
            </div>
            <p>{{ card.courseTitle }}</p>
            <h1 class="mt-3">{{ card.cost }}</h1>
            <p class="mt-3">{{ card.description }}</p>
          </header>
          <footer :class="footerClasses(index)">
            <div v-for="(item, iconIndex) in ['itemOne', 'itemTwo', 'itemThree']" :key="item" class="flex gap-4 mt-3">
              <div :class="iconClasses(index, iconIndex)">
                <Icon :icon="card[item + 'Icon']" width="24" height="24"/>
              </div>
              <div><p>{{ card[item] }}</p></div>
            </div>
            <div class="mt-10">
              <button class="text-black bg-white shadow-2xl uppercase px-5 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">
                Contact Us
              </button>
            </div>
          </footer>
        </article>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue';
import { reactive } from 'vue';

const cards = reactive([
  { courseTitle: 'Consultation', cost: 'Free', description: 'Your digital marketing efforts, instead of handling in-house.', itemOneIcon: 'mdi:plus', itemOne: 'Brand Design', itemTwoIcon: 'mdi:minus', itemTwo: 'Market Analysis', itemThreeIcon: 'mdi:minus', itemThree: 'Production' },
  { courseTitle: 'Design', cost: '$1500', description: 'Provide your business with a variety of digital solutions to promote.', itemOneIcon: 'mdi:plus', itemOne: 'Brand Design', itemTwoIcon: 'mdi:minus', itemTwo: 'Market Analysis', itemThreeIcon: 'mdi:minus', itemThree: 'Production' },
  { courseTitle: 'Design+Code', cost: '$3000', description: 'Help you hit your marketing goals and grow your business.', itemOneIcon: 'mdi:plus', itemOne: 'Brand Design', itemTwoIcon: 'mdi:minus', itemTwo: 'Market Analysis', itemThreeIcon: 'mdi:minus', itemThree: 'Production' },
]);

const cardClasses = (index) => [
  'p-6', 'border', 'border-gray-900', 'rounded', 'hover:bg-gray-900', 'group', 'transition-all', 'ease-in-out', 'duration-500',
  { 'rounded border md:border-r-0 md:rounded-left md:rounded-r-none': index === 0 },
  { 'border rounded md:rounded-none md:rounded-t bg-white group-hover:text-white': index === 1 },
  { 'rounded border md:rounded-none md:border-l-0 md:rounded-r': index === 2 },
];

const headerClasses = (index) => [
  'group-hover:text-white', 'transition-all', 'ease-in-out', 'duration-500',
];

const footerClasses = (index) => [
  'group-hover:text-white', 'transition-all', 'ease-in-out', 'duration-500',
];

const iconClasses = (cardIndex, iconIndex) => [
  'rounded-full', 'text-white', 'h-5', 'w-5', 'flex', 'items-center', 'justify-center', 'text-3xl',
  { 'bg-orange-200': (cardIndex === 0 && iconIndex !== 0) || (cardIndex === 1 && iconIndex === 2) },
  { 'bg-orange-500': !((cardIndex === 0 && iconIndex !== 0) || (cardIndex === 1 && iconIndex === 2)) },
];
</script>

<style>
/* Add additional styles here if needed */
</style>
