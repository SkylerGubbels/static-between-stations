<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import NavTabs from './components/NavTabs.vue';
import Socials from './components/Socials.vue';

function randomIntFromInterval(min: number, max: number) { // min and max included 
  return Math.floor(Math.random() * (max - min + 1) + min)
}

const images = [
{img: "src/assets/backgrounds/birdshot.png", title: "src/assets/titles/yellow.png"},
{img: "src/assets/backgrounds/control.png",  title: "src/assets/titles/white.png"},
{img:"src/assets/backgrounds/diner.png",  title: "src/assets/titles/orange.png"},
{img:"src/assets/backgrounds/escalator.png",  title: "src/assets/titles/orange.png"},
{img:"src/assets/backgrounds/laundromat.png", title: "src/assets/titles/blue.png"},
{img:"src/assets/backgrounds/planetarium.png", title: "src/assets/titles/blue.png"},
{img:"src/assets/backgrounds/skull.png", title: "src/assets/titles/blue.png"},
{img:"src/assets/backgrounds/stairwell.png", title: "src/assets/titles/orange.png"}
]

const idx = randomIntFromInterval(0,images.length - 1);
const backgroundImage = images[idx].img;
const title = images[idx].title;
</script>

<template>
  <div class="parentDiv"> 
    <div>
      <NavTabs class="navbar" :title="title"/>
    </div>
    <div class="video">
      <!-- https://codepen.io/dudleystorey/pen/BaPeZP-->
      <video poster="/src/assets/backgrounds/planetarium.png" id="bgvid" playsinline autoplay muted loop>
      <source  src="/src/assets/videos/backgroundwebm.webm" type="video/webm">
      <source src="/src/assets/videos/backgroundvid.mp4" type="video/mp4">

    </video>
  </div>
  <RouterView />
</div>
</template>

<style scoped>

.parentDiv {
  padding-left: 100px;
  padding-right: 100px;
}

@media (max-width: 1024px) {
  .parentDiv {
    padding-left: 10px;
    padding-right: 10px;
  }
}

.page {
 min-height: 100vh;
 min-width: 100vw;
}

.navbar {
  overflow: hidden;
  background-color: transparent;
  position: static;
  top: 0;
  width: 100%;
}

@media screen and (max-width: 1024px){
  .navbar {
  overflow: hidden;
  background-color: transparent;
  top: 0;
  width: 100%;
}
}

.title {
  min-height: 300px;
  min-width: 100vw;
  max-width:100vw
}

video { 
    position: fixed;
    top: 50%;
    left: 50%;
    min-width: 100%;
    min-height: 100%;
    width: auto;
    height: auto;
    z-index: -100;
    transform: translateX(-50%) translateY(-50%);
 background: url('\src\assets\backgrounds\planetarium.png') no-repeat;
  background-size: cover;
  transition: 1s opacity;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  background-color: transparent;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    padding-right: calc(var(--section-gap) / 2);
  }



  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
  }
}
</style>
