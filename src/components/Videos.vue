<script setup lang="ts">
import Socials from './Socials.vue';



</script>

<template>
    <div class="padding">
        <div>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/vM3dTFFFvrM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/nyWlE4LidJg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
    </div>
    <div class="socials"><Socials/></div>
    
</template>

<style scoped>

.padding {
    top: 100px;
}

.socials {
    top: 50px;
}

iframe {
   display: block;
   margin: 0 auto;
   width: 80%;
   height: 80vh;
   padding-bottom: 50px;
}

</style>