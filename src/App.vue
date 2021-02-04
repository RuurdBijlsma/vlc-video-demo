<template>
    <div id="app">
        <h1>VLC Video</h1>
        <vlc-video ref="player" class="player" dark
                   height="auto"
                   controls
                   src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"/>
        <h1>HTML Video</h1>
        <video class="player"
               height="auto"
               controls
               src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"/>
    </div>
</template>

<script>
import VlcVideo from "vlc-video";
// import VlcVideo from "./components/VlcVideo";

export default {
    name: 'App',
    components: {VlcVideo},
    mounted() {
        console.log(this.$refs.player);
    },
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

.player {
    width: 80%;
}
</style>
