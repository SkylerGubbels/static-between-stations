<script setup lang="ts">

import {ref} from "vue";

const photos: any = [
    {image: "src/assets/sketchfab/icebox.png", embed: "https://sketchfab.com/models/f96b503849f4477ea1501448d41f361a/embed?autostart=1&dnt=1"},
    {image: "src/assets/sketchfab/Cinderblocks.png", embed: "https://sketchfab.com/models/156888bf9f8f4ff69f347d6505f45b4f/embed?dnt=1&autostart=1"},
    {image: "src/assets/sketchfab/RuinsFire.png", embed: "https://sketchfab.com/models/4a6640785fac44bda0567b0dda2066e8/embed?autostart=1&dnt=1"},
    {image: "src/assets/sketchfab/Train.png", embed: "https://sketchfab.com/models/7d3a68adca2f46c198ca075f77b580d4/embed?autostart=1&dnt=1"},
    {image: "src/assets/sketchfab/wolfskull.png", embed: "https://sketchfab.com/models/fff98f1d39db4d3d84d9199c58e107af/embed?autostart=1&dnt=1"},
    {image: "src/assets/sketchfab/campfirebeach.png", embed: "https://sketchfab.com/models/d10994d04a434496b46657b1e141f41e/embed?dnt=1&autostart=1"},
];

const handleClick = (embedStr: string): void => {
    embed.value = embedStr;
}

const handleBack = () => embed.value = null;

const embed = ref<string | null>(null);

</script>

<template>
    <div v-if="embed" class="sketchfab-wrapper">
        <a class="backButton" @click="handleBack">{{`Back`}}</a>
        <div class="sketchfab-embed-wrapper"> 
            <iframe 
                title="Asset" 
                frameborder="0" 
                allowfullscreen 
                mozallowfullscreen="true" 
                webkitallowfullscreen="true" 
                allow="autoplay; fullscreen; xr-spatial-tracking" 
                xr-spatial-tracking 
                execution-while-out-of-viewport 
                execution-while-not-rendered 
                web-share 
                :src="embed"> 
            </iframe> 
        </div>
    </div>
    <div v-else>
        <div class="gallery">
        
        <div class="gallery-panel"
            v-for="photo in photos"
            @click="() => handleClick(photo.embed)"
            :key="photo.image">
        <img :src="photo.image">
        </div>
        </div>
    </div>
</template>

<style scoped>

h1 {
  font-family: "Fjalla One";
  color: white;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(20rem, 1fr));
    grid-gap: 1rem;
    max-width: 80rem;
    margin: 5rem auto;
    padding: 0 5rem;
  }

  .gallery-panel img {
    width: 100%;
    height: 22vw;
    object-fit: cover;
    border-radius: 0.75rem;
  }

  .gallery-panel img:hover {
    cursor: pointer;
  }

  img {
    -webkit-filter: brightness(100%);
}

img:hover {
    -webkit-filter: brightness(70%);
    -webkit-transition: all 0.2s ease;
    -moz-transition: all 0.2s ease;
    -o-transition: all 0.2s ease;
    -ms-transition: all 0.2s ease;
    transition: all 0.2s ease;
}

.sketchfab-wrapper {
    top: 150px;
}

iframe {
   display: block;
   margin: 0 auto;
   width: 80%;
   height: 80vh;
   padding-bottom: 50px;
}

.backButton {
    left: 10%;
    margin-bottom: 10px;
}

a {
    font-family: Monoton;
    color:white;
    font-size: 32px;
    text-align: right;
  }

</style>