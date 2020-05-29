<template>
  <div class="video-list">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <video-player class="video-player-box vjs-custom-skin" ref="videoPlayer" :options="playerOptions"></video-player>
        <Description></Description>
      </swiper-slide>
      <swiper-slide>
        <video-player class="video-player-box" ref="videoPlayer" :options="playerOptions2"></video-player>
        <Description></Description>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import Description from "@/components/home/description";
import { swiper, swiperSlide } from 'vue-awesome-swiper' 
export default {
  name: "VideoList",
  components: {
    Description,
    
  },
  data() {
    return {
      swiperOption: {
        direction: "vertical",
        autoHeight: true, //自动高度。设置为true时，wrapper和container会随着当前slide的高度而发生变化       
        height: window.innerHeight, // 高度设置，占满设备高度
        pagination: {
          el: ".swiper-pagination",
          clickable: true,            
        },
        
      },
      playerOptions: {
        // videojs options
        height: window.innerHeight,
        width: window.innerWidth,
        autoplay: true,
        muted: false,
        loop: true,
        preload:'auto',
        language: "en",
        playbackRates: [0.7, 1.0, 1.5, 2.0],
        sources: [
          {
            type: "video/mp4",
            src: "http://localhost:8181/3.mp4"
          }
        ]
      },
      
        playerOptions2: {
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
            src: "http://localhost:8181/2.mp4"
          }
        ]
      }
    };
  },
  
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