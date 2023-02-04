<script setup lang="ts">
import type { PropType } from 'vue';
import { RouterLink, RouterView, useRoute } from 'vue-router'

const props = defineProps({
    title: {
        type: String as PropType<string>,
        required: true,
        default: "src/assets/titles/yellow.png"
    }
})

const route = useRoute();
</script>

<template>
  <div class="parentDiv">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Fjalla+One">
      <nav>
        <RouterLink to="/"><span class="navFont">Home</span></RouterLink>
        <RouterLink to="/music"><span class="navFont">Music</span></RouterLink>
        <RouterLink to="/music"><span class="navFont">Videos</span></RouterLink>
        <RouterLink to="/assets"><span class="navFont">Free Assets</span></RouterLink>
        <RouterLink to="/contact"><span class="navFont">Contact</span></RouterLink>
     </nav>
</div>
</template>

<style scoped>

.parentDiv nav {
  padding-right: 100px;
}

.router-link-active span {
  text-decoration: underline;
}

.navFont {
  font-family: "Fjalla One";
  color: white;
}

.navFont span:hover {
  text-decoration: underline;
}

.bandName {
    max-width: 500px;
    min-width: 250px;
}

.parentDiv {
    background-color: transparent;
}


.title {
  min-height: 300px;
  min-width: 100vw;
  max-width:100vw
}


nav {
  font-size: 12px;
  text-align: center;
  background-color: transparent;
  float:right;
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
    place-items: center;
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
