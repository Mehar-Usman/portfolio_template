<template >
    <div class="grid grid-cols-2 lg:grid-cols-5 justify-center items-center gap-10 px-6 md:px-10 lg:px-20 xl:px-28">
        <div class="flex items-center justify-center" v-for="(img , index) in Images" :key="index" :class="{' col-span-2 lg:col-span-1 mx-auto md:mx-0' : index===4}">
            <img  :src="img.dynmicImg" alt="">
        </div>
    </div>
</template>
<script setup>
    import {reactive} from 'vue';
    const Images = reactive([
            {dynmicImg:'src/assets/Bitmap.png' , imgAlt:'img1'},
            {dynmicImg:'src/assets/Bitmap (1).png' , imgAlt:'img2'},
            {dynmicImg:'src/assets/Bitmap (2).png' , imgAlt:'img3'},
            {dynmicImg:'src/assets/Bitmap (3).png' , imgAlt:'img4'},
            {dynmicImg:'src/assets/Bitmap (4).png' , imgAlt:'img5'},
    ]);
</script>
<style >
    
</style>