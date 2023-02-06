<script setup lang="ts">


</script>

<template>
  <div class="socials">
    <a href="https://www.instagram.com/staticbetweenstationsmusic/" target="_blank"><img src="@/assets/icons/icons8-instagram.svg"/></a>
    <a href="https://www.youtube.com/@staticbetweenstations" target="_blank"><img src="@/assets/icons/icons8-youtube-logo.svg"/></a>
    <a href="https://open.spotify.com/artist/0VDm6NTbq4c5jfLlwAAwIi" target="_blank"><img src="@/assets/icons/icons8-spotify.svg"/></a>
    <a href="https://www.tiktok.com/@staticbetweenstations" target="_blank"><img src="@/assets/icons/icons8-tiktok.svg"/></a>
    <a href="https://www.facebook.com/staticbetweenstations" target="_blank"><img src="@/assets/icons/icons8-facebook.svg"/></a>
  </div>
</template>

<style scoped>

img {
    padding: 10px;
    max-width: 75px;
    max-height: 75px;
}

@media (hover: hover) {
  img:hover {
    background-color: #b9b9b923;
    cursor: pointer;
  }
}

.socials {
   left: 0;
   bottom: 20px;
   width: 100%;
   text-align: center;
}

</style>