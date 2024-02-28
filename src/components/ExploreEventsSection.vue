<template >
    <div class="bg-gray-900 py-10">
    <div>
        <p class="text-orange-500 text-center text-2xl">Events</p>
        <p class="text-4xl text-center font-900 text-white">Explore Future <br> Conferences</p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 px-6 md:px-10 lg:px-20  xl:px-28 py-8 md:py-12 lg:py-16 ">
        <div class="border border-gray-700 shadow-2xl rounded p-6" v-for="(card , index) in cards" :key="index"> 
            <header class="pb-6">
                <div class="flex gap-2 items-center">
                    <div>
                        <p class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl  font-900 text-white">{{ card.title }}</p>
                    </div>
                    <div class="">
                        <h3 class="w-3/4 text-white">{{ card.eventDate }}</h3>
                    </div>
                </div>
                <div class="flex items-center  gap-1 mt-3">
                    <div>
                        <img src="../assets/clock.svg" alt="">
                    </div>
                    <div>
                        <p class="text-sm font-light text-white">{{ card.eventTime }}</p>
                    </div>
                </div>
            </header>
            <hr class="border-t-1 w-full border-gray-700">
            <footer class="mt-6">
                <div >
                    <h1 class="text-white">{{ card.eventSubtitle }}</h1>
                    <p class="text-white mt-3">{{ card.subtitleDescription }}</p>
                </div>
                <div>
                    <button class="mt-5 text-white hover:shadow-2xl uppercase px-4 py-2 border-2 border-gray-500 rounded-xl transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">Explore Now</button>
                </div>
            </footer>
        </div>
    </div>
    <div class="flex justify-center">
        <button class="mt-5 text-white uppercase shadow-2xl px-4 py-2 border-2 border-gray-500 rounded-xl transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">Explore More</button>
    </div>
</div>

</template>
<script setup>
    import {reactive} from 'vue';
    const cards = reactive([
        {title:'3', eventDate:'November 2021',eventTime:'9:00 am - 3:00 pm',eventSubtitle:'Design Weeks',subtitleDescription:'Digital agency is a business you hire to outsource your digital.'},
        {title:'3', eventDate:'November 2021',eventTime:'9:00 am - 3:00 pm',eventSubtitle:'Design Weeks',subtitleDescription:'Digital agency is a business you hire to outsource your digital.'},
        {title:'3', eventDate:'November 2021',eventTime:'9:00 am - 3:00 pm',eventSubtitle:'Design Weeks',subtitleDescription:'Digital agency is a business you hire to outsource your digital.'},
    ])
</script>
<style >
    
</style>