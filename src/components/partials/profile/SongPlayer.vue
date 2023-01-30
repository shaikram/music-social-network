<script setup>
import { onMounted } from 'vue'
import APlayer from "aplayer"
import 'aplayer/dist/APlayer.min.css'


onMounted(() => { 
    thePlayer()
})

const thePlayer = () => {
  new APlayer({
    container: document.getElementById("aplayer"),
    audio: [
            {
                name: "First Song",
                artist: "artist",
                url: "/music/into-the-night-20928.mp3",
                cover: "cover.jpg",
            },
            {
                name: "Second Song",
                artist: "artist",
                url: "/music/just-relax-11157.mp3",
                cover: "cover.jpg",
            },
    ],
  })
}

</script>

<template>
  <div class="bg-green-500 rounded">
    <div id="aplayer"></div>
  </div>
</template>
