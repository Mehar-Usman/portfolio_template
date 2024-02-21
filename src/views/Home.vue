<template>
    <div>
        <NavbarComp/>
        <ModernStudio/>
        <AboutUs/>
        <HowWeWork/>
        <VideoReelSection/>
        <Features/>
    </div>
</template>
<script>
import AboutUs from '../components/AboutUs.vue';
import HowWeWork from '../components/HowWeWork.vue';
import ModernStudio from '../components/ModernStudio.vue';
import NavbarComp from '../components/NavbarComp.vue';
import VideoReelSection from '../components/VideoReelSection.vue'
import Features from '../components/Features.vue'
export default{
    components:{
    NavbarComp,
    ModernStudio,
    AboutUs,
    HowWeWork,
    VideoReelSection,
    Features
}
}


</script>
<style >
    
</style>