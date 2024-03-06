<template>
    <div class='bg-orange-100 px-6 md:px-10 lg:px-20 py-12 xl:px-28'>
        <header>
            <p class='text-center font-900 text-5xl'>Contact Us</p>
        </header>
        <div class="grid grid-cols-1 md:grid-cols-3 py-16 gap-10 md:gap-0">
            <div v-for="(card, index) in ContactUsCards" :key="index">
                <article>
                    <div :class="[
                'p-8 border border-gray-900 rounded shadow-2xl hover:bg-gray-900 group transition-all ease-in-out duration-500  ',
                { 'border md:border-t md:border-b md:border-l-0 md:border-r-0': index === 1 },
                { 'rounded  md:rounded-none md:rounded-l': index === 0 },
                { 'rounded md:rounded-none': index === 1 },
                { 'rounded md:rounded-none md:rounded-r': index === 2 },
            ]">
                        <div class="flex gap-4 items-center">
                            <div
                                class="bg-orange-500 w-10 h-10 rounded-full flex items-center justify-center group-hover:translate-x-5 transition-all duration-500 ease-in-out group-hover:shadow-2xl group-hover:bg-white">
                                <!-- Dynamic Icon using Iconify -->
                                <Icon
                                    class="text-white group-hover:text-gray-900 ease-in-out transition-all duration-500"
                                    :icon="card.icon" width="24" height="24" />
                            </div>
                            <div>
                                <p
                                    class="text-orange-500 group-hover:text-white group-hover:translate-x-5 transition-all duration-500 ease-in-out">
                                    {{ card.title }}</p>
                            </div>
                        </div>
                        <section class="mt-4">
                            <p
                                class="mt-3 group-hover:text-white group-hover:translate-x-5 transition-all duration-500 ease-in-out">
                                {{ card.content }}</p>
                        </section>
                    </div>
                </article>
            </div>
        </div>
        <div class="bg-[#ef6d58]">
            <div class="grid grid-cols-1 md:grid-cols-2 px-10 flex-col items-center gap-10">
                <div class="">
                    <p class="text-white text-4xl font-700">We’re Help
                        To Build Your
                        Dream Project</p>
                    <p class="text-white text-sm mt-4">A digital agency is a business you hire to outsource your digital marketing efforts, instead of
                        handling in-house.
                    </p>
                    <div class="mt-4">
                        <button class="text-black bg-white shadow-2xl uppercase px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">
                  Conatct Us
                </button>
                    </div>
                </div>
                <div class="">
                    <img src="../assets/contactUs.png" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { reactive } from 'vue';
import { Icon } from '@iconify/vue';

const ContactUsCards = reactive([
    { icon: 'mdi:phone', title: 'Phone ', content: '+1 (234) 567-89-00', },
    { icon: 'mdi:email', title: 'Email', content: 'info@agency.com', },
    { icon: 'mdi:location', title: 'Address', content: '2247 Lunetta Street, TX 76301', },
]);
</script>

<style scoped></style>