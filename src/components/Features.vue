<template>
    <div class="bg-orange-100">
        <div class=" grid  grid-cols-1 md:grid-cols-2 px-6 md:px-10 lg:px-20 py-20 xl:px-28 gap-20 justify-center items-center">
            <div class="">
                <article>
                <p class="text-orange-500 text-2xl uppercase">features</p>
                <h1 class="text-3xl lg:text-4xl w-full lg:w-3/4 font-900 text-gray-900 mt-5">Give Your Site A New Look</h1>
                <p class="w-full text-justify lg:w-3/4 mt-5 mb-10">Service range including technical skills, design, business understanding.</p>
                <div class="flex gap-3 mt-4 items-center " v-for="(list ,index) in lists" :key="index" >
                    <div class="bg-orange-500  h-8 w-8 flex items-center justify-center rounded-full">   
                        <img :src="list.icon" alt="">
                    </div>
                    <div>
                        <p class="font-light text-sm">{{ list.content }}</p>
                    </div>
                </div>
            </article>
        </div>
        <div class="">
            <img src="../assets/featuresMain.png" alt="">
        </div>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-2 px-6 md:px-10 lg:px-20 py-20 xl:px-28 gap-20 justify-center items-center">
        <div class="">
            <p class="text-2xl font-light text-orange-500 uppercase">features</p>
            <p class=" w-full lg:w-3/4 mt-5">Long run, and work as an extension of the merchant's team.</p>
            <button class="mt-5 text-black bg-white uppercase px-6 py-2 border-2 border-gray-500 rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">Read More</button>
        </div>
        <div class="block lg:flex items-end">
            <article class="p-6 bg-white rounded">
                <div class="bg-orange-500 p-[1px] h-16 w-16 flex items-center justify-center rounded-full">
                    <img class=" rounded-full" src="../assets/featuresIcon.png" alt="">
                </div>
                <h2 class="mt-5">professional</h2>
                <p class="text-sm mt-5 font-light">Full service range including technical skills, design.</p>
            </article>
            <article class="p-5 border border-gray-300">
                    <h2>Accessibility</h2>
                        <p class="mt-3 text-sm font-light">Business understanding, ability to put themselves.</p>
            </article>
        </div>
    </div>
</div>
</template>
<script setup>
    import {reactive} from 'vue';

    const lists = reactive([
        {icon:'src/assets/path.png', content:'Range including technical skills'},
        {icon:'src/assets/path.png', content:'Business understanding'},
        {icon:'src/assets/path.png', content:'Partner on the long run'},
    ]);
</script>
<style>
    
</style>