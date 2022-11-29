<template>
  <div :class="$style.container">
    <img
      src="https://mocossi.com/static/media/group_2470@3x.c8019e7eeb08f2415e9f.jpg"
      alt=""
      class="bg"
    />
    <div class="header">
      <h2>RoadMap</h2>
    </div>

    <div class="content">
      <swiper :slides-per-view="3" :space-between="20" ref="myswiper">
        <swiper-slide v-for="item in datas" :key="item.key">
          <RoadMapItem :data="item"></RoadMapItem>
        </swiper-slide>
        <div :class="$style.navigations">
          <div :class="$style.left" @click="onPrev"></div>
          <div :class="$style.right" @click="onNext"></div>
        </div>
      </swiper>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive, ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import RoadMapItem from "./RoadMapItem.vue";
import "swiper/css";
const datas = reactive([
  {
    key: 1,
    title: "Story",
    img: "	https://mocossi.com/static/media/completed.423571b6c9d07cded421473e125242cc.svg",
    text: `<p>Land sales<br>Land web mobile version<br>Official land map<br>Public sale through LBE<br>Encyclopedia<br>Moconomics<br>Eternl wallet integration<br>Flashito sales</p>`,
  },
  {
    key: 2,
    title: "Breeding",
    img: "https://mocossi.com/static/media/inprogress.be318b56e752c0b5ea3a.png",
    text: `<p>Scholarship program<br>Physical product online store<br>In-house marketplace</p>`,
  },
  {
    key: 3,
    title: "Mocossi Planet",
    img: "https://mocossi.com/static/media/planned.f7a6dacd8d6bdbc31bf3.png",
    text: `<p>Token airdrop<br>Mocossi Planet Game - MVP version<br>MCOS dashboard<br>DAO vote (25,000 ITO2 threshold)</p>`,
  },
  {
    key: 4,
    title: "Story",
    img: "	https://mocossi.com/static/media/completed.423571b6c9d07cded421473e125242cc.svg",
    text: `<p>Land sales<br>Land web mobile version<br>Official land map<br>Public sale through LBE<br>Encyclopedia<br>Moconomics<br>Eternl wallet integration<br>Flashito sales</p>`,
  },
  {
    key: 5,
    title: "Breeding",
    img: "https://mocossi.com/static/media/inprogress.be318b56e752c0b5ea3a.png",
    text: `<p>Scholarship program<br>Physical product online store<br>In-house marketplace</p>`,
  },
  {
    key: 6,
    title: "Mocossi Planet",
    img: "https://mocossi.com/static/media/planned.f7a6dacd8d6bdbc31bf3.png",
    text: `<p>Token airdrop<br>Mocossi Planet Game - MVP version<br>MCOS dashboard<br>DAO vote (25,000 ITO2 threshold)</p>`,
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
  flex: 1 1;
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
      z-index: 1;
    }
  }
}
</style>
