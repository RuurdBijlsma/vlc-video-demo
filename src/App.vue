<template>
    <div id="app">
        <h1>VLC Video</h1>
        <vlc-video height="300" controls ref="player" class="player" dark
                   src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"/>
        <h1>HTML Video</h1>
        <video height="300" controls class="player"
               src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"/>
    </div>
</template>

<script>
import VlcVideo from "vlc-video";

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
</style>
