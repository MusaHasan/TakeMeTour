<template>
    <div class="custom_video_player">
        <video  :src="source" ref="htmlVideo" v-if="isAnMp4"></video>
        <iframe class="vidodiv" :src="source" ref="iframeVideo" v-if="!isAnMp4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />
        <div class="custom_video_player--controls">
            <div class="custom_video_player--controls-playpause"></div>
                <div class="custom_video_player--controls-track">
                    <div class="custom_video_player--controls-track_seek"></div>
                </div>
            <div class="custom_video_player--controls-elapsedtime"></div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        source:{
            type: String,
            required: true
        }
	},
    data:()=>({
        ready: false,
        elapsedTime: '00:00',
        volumeLevel: 50,
        isPlaying: false
    }),
    mounted(){
        this.ready = true;
        let HTMLvideo = this.$refs['htmlVideo'];
    },
    computed: {
        isAnMp4() {
            return this.source.includes('.mp4');
        }
    },
    methods: {
        stateToggle() {},
        scrobble() {},
        fullscreen() {}
    }
}
</script>

<style>
    .custom_video_player{
        width: 100%;
        height: auto;
    }
    .vidodiv{
        width: 100%;
        height: 380px;
        border-radius: 12px;
        margin: 0 -20px;
    }
</style>