<template>
        <div v-for="video in videos" :key="video.title">
                <video class="video-js" controls preload="auto">
                        <source v-bind:src="videoinicio.src" type="video/mp4">
                </video>
        </div>
</template>
<script>
export default {
        data: () => ({
                videos: [
                        { title: "video-inicio", src: "../../assets/videos/video-inicio.mp4", desc: "vídeo inicial" }
                ]
        })
}
</script>
