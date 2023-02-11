<script setup lang="ts">
import YoutubeVideo from '@/components/YoutubeVideo.vue';
import Socials from '@/components/Socials.vue';
</script>

<template>
  <div class="titleRight">
    <h1>Static<br>Between<br>Stations</h1>
    <div class="newSingle"><span>New single // <a href="https://www.youtube.com/watch?v=vM3dTFFFvrM">Take a Deep Breath</a></span></div>
  </div>

  <Socials class="fixed"/>
</template>

<style scoped>

  .fixed {
    position: fixed;
  }

  .titleRight {
    top:200px
  }

  .newSingle {
    float: right;
    font-family: "Fjalla One";
    color: white;
    font-size: 32px;
  }

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
      font-size: 10vw;
      text-align: center;
    }

    .newSingle {
      text-align: center;
      float:none;
      font-size: 5vw;
      top:25px;
    }
    .titleRight {
      top: 100px
    }
  }
  
</style>