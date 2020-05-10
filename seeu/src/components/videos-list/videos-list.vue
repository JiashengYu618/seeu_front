<template>
  <div class="video-list">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <video-player class="video-player-box" ref="videoPlayer" :options="playerOptions"></video-player>
        <Description></Description>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import Description from "@/components/home/description";
export default {
  name: "VideoList",
  components: {
    Description
  },
  data() {
    return {
      swiperOption: {
        direction: "vertical",
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        }
      },
      playerOptions: {
        // videojs options
        height: window.innerHeight,
        width: window.innerWidth,
        autoplay: true,
        muted: false,
        loop: true,
        language: "en",
        playbackRates: [0.7, 1.0, 1.5, 2.0],
        sources: [
          {
            type: "video/mp4",
            src: "http://localhost:8181/3.mp4"
          }
        ]
      }
    };
  }
};
</script>

<style lang='stylus' scoped>
.video-list {
  height: 100%;
  background-color: #000;
  z-index: -100;

  .swiper-container {
    height: 100%;

    .swiper-wrapper {
      height: 100%;

      .swiper-slide {
        height: 100%;
        color: #ffffff;
        position: relative;
        .description {
          position: absolute;
          bottom:80px;
          left:22px;
         
        }
      }
    }
  }
}
</style>