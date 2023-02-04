<script setup lang="ts">
import YoutubeVideo from '@/components/YoutubeVideo.vue';
</script>

<template>
  <div class="titleRight">
    <h1>Static<br>Between<br>Stations</h1>
  </div>
  <div class="newSingle"><span>New single: Take a Deep Breath</span></div>
</template>

<style scoped>
  @font-face {
    font-family: "Monoton";
    src: url("@/assets/fonts/Monoton-Regular.ttf");
  }
  
    h1 {
    font-family: Monoton;
    color:white;
    font-size: 130px;
    text-align: right;
    line-height: 150%;
  }

  @media screen and (max-width: 1024px){
      h1 {
      font-family: Monoton;
      color:white;
      font-size: 10vw;
      text-align: center;
      line-height: 150%;
    }
    .titleRight {
      top: 100px
    }
  }
  
</style>