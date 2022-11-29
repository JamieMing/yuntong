<template>
  <div class="container">
    <video
      src="https://mocossi.com/static/media/mocossi_final_v2.9371ce9698661d644e3e.mp4"
      autoplay
      loop
      muted
      class="video"
    ></video>
    <div class="overlay"></div>
    <div class="wrapper">
      <img
        src="https://mocossi.com/static/media/play.2aa0c2077ed1b85b1e40ee2e25eb346a.svg"
        alt=""
        class="play-button"
      />
      <h2>The first P&E virtual pet and farming simulation game on Cardano</h2>
      <div class="button-wrappr">
        <div class="red-button">
          <p>Breed now</p>
        </div>
        <div class="yellow-button">
          <p>Get Mcos</p>
        </div>
      </div>
      <div class="cards-wrapper">
        <BannerCardItem v-for="item in datas" :key="item.text" :data="item" />
      </div>
      <p class="desc">*Data obtained from opencnft.io</p>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive } from "vue";
import BannerCardItem from "./BannerCardItem.vue";
import image4 from "@/assets/images/image4.png";
const datas = reactive([
  {
    img: "https://mocossi.com/static/media/1.5831eb5762a89946f030.png",
    text: "Floor Price (ITO)",
  },
  {
    img: "https://mocossi.com/static/media/2.a5aef679cdadc3f5d218.png",
    text: "Floor Price (ITO)2",
  },
  {
    img: "https://mocossi.com/static/media/3.5f7aecdf00aacf2a0391.png",
    text: "Floor Price (ITO)3",
  },
  {
    img: image4,
    text: "Floor Price (ITO)4",
  },
  {
    img: "https://mocossi.com/static/media/lands.682c6036d009c038289a.gif",
    text: "Floor Price (ITO)5",
  },
]);
</script>
<style lang="less" scoped>
@import "@/assets/base.less";
.container {
  background-color: #350028;
  height: 1080px;
  width: var(--global-width);
  overflow: hidden;
  position: relative;
  .video {
    position: absolute;
    z-index: 1;
    top: 0;
    left: 0;
    width: 100%;
  }
  .overlay {
    background: linear-gradient(180deg, rgba(53, 0, 40, 0), #350028);
    bottom: 0;
    height: 600px;
    left: 0;
    position: absolute;
    right: 0;
    z-index: 1;
  }
  .wrapper {
    align-items: center;
    bottom: 0;
    display: flex;
    flex-direction: column;
    left: 0;
    padding-top: 276px;
    position: absolute;
    right: 0;
    top: 0;
    z-index: 2;
    h2 {
      color: #fff;
      font-family: iCiel Cadena;
      font-size: 48px;
      line-height: 66px;
      margin: 12px 20px 32px;
      padding-top: 40px;
      text-align: center;
      text-shadow: -3px -3px 0 #c0346a, -3px -2px 0 #c0346a, -3px -1px 0 #c0346a,
        -3px 0 0 #c0346a, -3px 1px 0 #c0346a, -3px 2px 0 #c0346a,
        -3px 3px 0 #c0346a, -2px -3px 0 #c0346a, -2px -2px 0 #c0346a,
        -2px -1px 0 #c0346a, -2px 0 0 #c0346a, -2px 1px 0 #c0346a,
        -2px 2px 0 #c0346a, -2px 3px 0 #c0346a, -1px -3px 0 #c0346a,
        -1px -2px 0 #c0346a, -1px -1px 0 #c0346a, -1px 0 0 #c0346a,
        -1px 1px 0 #c0346a, -1px 2px 0 #c0346a, -1px 3px 0 #c0346a,
        0 -3px 0 #c0346a, 0 -2px 0 #c0346a, 0 -1px 0 #c0346a, 0 0 0 #c0346a,
        0 1px 0 #c0346a, 0 2px 0 #c0346a, 0 3px 0 #c0346a, 1px -3px 0 #c0346a,
        1px -2px 0 #c0346a, 1px -1px 0 #c0346a, 1px 0 0 #c0346a,
        1px 1px 0 #c0346a, 1px 2px 0 #c0346a, 1px 3px 0 #c0346a,
        2px -3px 0 #c0346a, 2px -2px 0 #c0346a, 2px -1px 0 #c0346a,
        2px 0 0 #c0346a, 2px 1px 0 #c0346a, 2px 2px 0 #c0346a, 2px 3px 0 #c0346a,
        3px -3px 0 #c0346a, 3px -2px 0 #c0346a, 3px -1px 0 #c0346a,
        3px 0 0 #c0346a, 3px 1px 0 #c0346a, 3px 2px 0 #c0346a, 3px 3px 0 #c0346a;
    }
    .play-button {
      background: none;
      border: none;
      cursor: pointer;
    }
    .button-wrappr {
      width: 600px;
      display: flex;
      justify-content: center;
    }
    .cards-wrapper {
      //   width: 80%;
      //   margin: 20px auto;
      display: flex;
      flex-direction: row;
      justify-content: center;
      min-height: 372px;
    }
    .desc {
      color: #fff;
      font-weight: bold;
      font-size: 18px;
    }
  }
}
</style>
