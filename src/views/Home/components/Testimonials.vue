<template>
  <div :class="$style.container">
    <img
      src="https://mocossi.com/static/media/group_2460@2x.8701d6bf90e74fbc56e4.jpg"
      alt=""
      class="bg"
    />
    <div class="header">
      <h2>Testimonials</h2>
    </div>
    <div class="content">
      <swiper :slides-per-view="3" :space-between="20" ref="myswiper">
        <swiper-slide v-for="item in datas" :key="item.key">
          <TestimonialsItem :data="item"></TestimonialsItem>
        </swiper-slide>
      </swiper>
      <div :class="$style.navigations" style="bottom: -80px">
        <div :class="$style.left" @click="onPrev"></div>
        <div :class="$style.right" @click="onNext"></div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { Swiper, SwiperSlide } from "swiper/vue";
import { reactive, ref } from "vue";
import type { ItemType } from "./TestimonialsItem.vue";
import TestimonialsItem from "./TestimonialsItem.vue";
import "swiper/css";

const datas = reactive<ItemType[]>([
  {
    text: `Really love the community and continuous updates from the team. Looking forward to the development of this project. P&amp;E, breeding, token airdrop all to come this year.`,
    username: "@HK_pxlz",
    img: "https://mocossi.com/static/media/2.f1131df5f69c03e475c9.jpg",
  },
  {
    text: `Really love the community and continuous updates from the team. Looking forward to the development of this project. P&amp;E, breeding, token airdrop all to come this year.`,
    username: "@HK_pxlz",
    img: "https://mocossi.com/static/media/2.f1131df5f69c03e475c9.jpg",
  },
  {
    text: `Really love the community and continuous updates from the team. Looking forward to the development of this project. P&amp;E, breeding, token airdrop all to come this year.`,
    username: "@HK_pxlz",
    img: "https://mocossi.com/static/media/2.f1131df5f69c03e475c9.jpg",
  },
  {
    text: `Really love the community and continuous updates from the team. Looking forward to the development of this project. P&amp;E, breeding, token airdrop all to come this year.`,
    username: "@HK_pxlz",
    img: "https://mocossi.com/static/media/2.f1131df5f69c03e475c9.jpg",
  },
  {
    text: `Really love the community and continuous updates from the team. Looking forward to the development of this project. P&amp;E, breeding, token airdrop all to come this year.`,
    username: "@HK_pxlz",
    img: "https://mocossi.com/static/media/2.f1131df5f69c03e475c9.jpg",
  },
  {
    text: `Really love the community and continuous updates from the team. Looking forward to the development of this project. P&amp;E, breeding, token airdrop all to come this year.`,
    username: "@HK_pxlz",
    img: "https://mocossi.com/static/media/2.f1131df5f69c03e475c9.jpg",
  },
]);
const myswiper = ref();
const onNext = () => {
  myswiper.value.$el.swiper.slideNext();
};
const onPrev = () => {
  myswiper.value.$el.swiper.slidePrev();
};
</script>
<style module lang="less">
@import "@/assets/base.less";
.container {
  background-color: #350028;
  display: flex;
  flex: 1;
  flex-direction: column;
  min-height: 960px;
  width: var(--global-width);
  margin-top: -1px;
  :global {
    .bg {
      background-color: transparent;
      position: absolute;
      width: var(--global-width);
      z-index: 1;
    }
    .header {
      align-items: center;
      display: flex;
      flex-direction: column;
      margin: 0 0 66px;
      z-index: 2;
      h2 {
        color: #fff;
        font-family: iCiel Cadena;
        font-size: 48px;
        line-height: 66px;
        padding-top: 40px;
        text-align: center;
        text-shadow: -3px -3px 0 #c0346a, -3px -2px 0 #c0346a,
          -3px -1px 0 #c0346a, -3px 0 0 #c0346a, -3px 1px 0 #c0346a,
          -3px 2px 0 #c0346a, -3px 3px 0 #c0346a, -2px -3px 0 #c0346a,
          -2px -2px 0 #c0346a, -2px -1px 0 #c0346a, -2px 0 0 #c0346a,
          -2px 1px 0 #c0346a, -2px 2px 0 #c0346a, -2px 3px 0 #c0346a,
          -1px -3px 0 #c0346a, -1px -2px 0 #c0346a, -1px -1px 0 #c0346a,
          -1px 0 0 #c0346a, -1px 1px 0 #c0346a, -1px 2px 0 #c0346a,
          -1px 3px 0 #c0346a, 0 -3px 0 #c0346a, 0 -2px 0 #c0346a,
          0 -1px 0 #c0346a, 0 0 0 #c0346a, 0 1px 0 #c0346a, 0 2px 0 #c0346a,
          0 3px 0 #c0346a, 1px -3px 0 #c0346a, 1px -2px 0 #c0346a,
          1px -1px 0 #c0346a, 1px 0 0 #c0346a, 1px 1px 0 #c0346a,
          1px 2px 0 #c0346a, 1px 3px 0 #c0346a, 2px -3px 0 #c0346a,
          2px -2px 0 #c0346a, 2px -1px 0 #c0346a, 2px 0 0 #c0346a,
          2px 1px 0 #c0346a, 2px 2px 0 #c0346a, 2px 3px 0 #c0346a,
          3px -3px 0 #c0346a, 3px -2px 0 #c0346a, 3px -1px 0 #c0346a,
          3px 0 0 #c0346a, 3px 1px 0 #c0346a, 3px 2px 0 #c0346a,
          3px 3px 0 #c0346a;
      }
    }

    .content {
      padding: 0 160px;
      z-index: 1;
    }
  }
}
</style>
