<script setup lang="ts">
import Socials from './Socials.vue';

import takeadeepbreath_wav from "@/assets/music/takeadeepbreathwav.wav";
import takeadeepbreath_mp3 from "@/assets/music/takeadeepbreathmp3.mp3";
import takeadeepbreath__i_wav from "@/assets/music/takeadeepbreathinstrumentalwav.wav";
import takeadeepbreath_i_mp3 from "@/assets/music/takeadeepbreathinstrumentalmp3.mp3";

import sinkintome_wav from "@/assets/music/sinkintomewav.wav";
import sinkintome_mp3 from "@/assets/music/sinkintomemp3.mp3";
import sinkintome_i_wav from "@/assets/music/sinkintomeinstrumentalwav.wav";
import sinkintome_i_mp3 from "@/assets/music/sinkintomeinstrumentalmp3.mp3";



</script>

<template>
    <iframe style="border-radius:12px" src="https://open.spotify.com/embed/artist/0VDm6NTbq4c5jfLlwAAwIi?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    
    <div class="downloads">
        <div class="divider" text-position="right">Downloads</div>
        <div class="content">
            <img src="@/assets/albums/takeadeepbreath.png"/>
            <div>
                <h1>Take a Deep Breath</h1>
                <p>Full song download: <a :href="takeadeepbreath_wav" download>wav</a> // <a :href="takeadeepbreath_mp3" download>mp3</a></p>
                <p>Instrumental: <a :href="takeadeepbreath__i_wav" download>wav</a> // <a :href="takeadeepbreath_i_mp3" download>mp3</a></p>
            </div>
        </div>
        <div class="content song">
            <img src="@/assets/albums/sinkintome.png"/>
            <div>
                <h1>Sink Into Me</h1>
                <p>Full song download: <a :href="sinkintome_wav" download>wav</a> // <a :href="sinkintome_mp3" download>mp3</a></p>
                <p>Instrumental: <a :href="sinkintome_i_wav" download>wav</a> // <a :href="sinkintome_i_mp3" download>mp3</a></p>
            </div>
        </div>
    </div>

    <Socials class="paddingTop"/>
</template>

<style scoped>

    .paddingTop {
        top: 50px;
    }

    .content {
        text-align: center;
    }

    iframe {
        top: 100px;
    }

    img {
        max-width: 250px;
    }

    .downloads {
        padding-top: 100px;
    }

    h1 {
        font-family: "Fjalla One";
        color: white;
    }

    p {
        font-family: "Fjalla One";
        color: white;
        padding-top: 10px;
    }

    .song {
        padding-top: 50px;
    }

    .divider {
        display: flex;
        align-items: center;
        color:white;
        font-size: 42px;
        font-family: "Fjalla One";
    }

    .divider:before,
    .divider:after {
    content: '';
        flex: 0 1 100%;
        border-bottom: 5px solid #ffffff;
        border-radius: 5px;
        margin: 0 1rem;
    }

    .divider:before {
        margin-left: 0;
    }

    .divider:after {
        margin-right: 0;
    }

</style>