<template>
    <div class='bg-orange-100 px-6 md:px-10 lg:px-20 py-12 xl:px-28'> 
        <div class='grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 md:gap-10 lg:gap-12'>
            <div class=''>
                <p class='text-4xl font-700 '>Agency</p>
            </div>
            <div>
                <p class='text-2xl text-orange-500'>MENU</p>
                <div class="mt-3">
                    <ul>
                        <li><router-link to="/">About</router-link></li>
                        <li><router-link to="/">Service</router-link></li>
                        <li><router-link to="/">Blog</router-link></li>
                        <li><router-link to="/">Contact</router-link></li>
                    </ul>
                </div>
            </div>
            <div>
                <p class='text-2xl text-orange-500'>Service</p>
                <div class="mt-3">
                    <ul>
                        <li><router-link to="/">Design</router-link></li>
                        <li><router-link to="/">Development</router-link></li>
                        <li><router-link to="/">Markeeting</router-link></li>
                        <li><router-link to="/">See More</router-link></li>
                    </ul>
                </div>
            </div>
            <div>
                <div class="flex gap-2">
                    <div class="bg-[#ef6d58] h-10 w-10 flex rounded-full items-center justify-center">
                        <Icon class="text-white" icon="mdi:facebook" width="24" height="24" />
                    </div>
                    <div class="bg-[#ef6d58] h-10 w-10 flex rounded-full items-center justify-center">
                        <Icon class="text-white" icon="mdi:twitter" width="24" height="24" />
                    </div>
                    <div class="bg-[#ef6d58] h-10 w-10 flex rounded-full items-center justify-center">
                        <Icon class="text-white" icon="mdi:instagram" width="24" height="24" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { Icon } from '@iconify/vue';


</script>
<style>
    
</style>