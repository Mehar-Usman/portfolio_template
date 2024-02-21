<template >
    <div class="bg-orange-100 py-14">
        <AboutUsHeader/>
        <div class="grid grid-cols-1 md:grid-cols-2 px-6 md:px-10 lg:px-20 py-20 xl:px-28 gap-20 justify-center items-center">
            <div>
                <img src="../assets/aboutPic.png" alt="">
            </div>
            <div>
                <article>
                    <p class="text-orange-500 text-2xl uppercase">About</p>
                    <h1 class= " md:text-3xl lg:text-5xl w-full lg:w-3/4 font-900 text-gray-900 mt-5">An Experience Design Agency</h1>
                    <p class="my-5 font-semibold text-gray-900">Provides a full service range</p>
                    <p class="w-full text-justify  lg:w-3/4 ">Ability to put themselves in the merchant's shoes. It is meant to partner on the long run, and work as an extension of the merchant's team.</p>
                    <button class=" mt-5 text-black bg-white uppercase px-6 py-2 border-2 border-gray-500  rounded transition-all ease-in-out font-semibold hover:border-white hover:scale-110 duration-500 hover:bg-gray-900 hover:text-white">about us</button>
                </article>
            </div>
        </div>
        <AboutUsFooterCards/>
    </div>
</template>
<script>
import AboutUsFooterCards from './AboutUsFooterCards.vue';
import AboutUsHeader from './AboutUsHeader.vue';

export default {
    components: { AboutUsHeader, AboutUsFooterCards }
}
</script>
<style >
    
</style>