<template>
  <div :class="$style.container">
    <img
      src="https://mocossi.com/static/media/group_2463@3x.04be4cca792900fb6b45.jpg"
      alt=""
      class="bg"
    />
    <div class="header">
      <h2>Story & Gameplay</h2>
    </div>
    <div class="tabs">
      <div
        class="tab-item"
        v-for="item in tabs"
        :key="item.title"
        @click="
          () => {
            onChangeTab(item.title);
          }
        "
      >
        <button
          :class="['tab-item-button', activeItem == item.title ? 'active' : '']"
        >
          <span>{{ item.title }}</span>
        </button>
      </div>
    </div>
    <div class="content">
      <!-- <div class="wrapper"> -->
      <img :src="current.img" alt="" class="img" />
      <div class="desc">
        <p>{{ current.content }}</p>
      </div>

      <!-- </div> -->
    </div>
  </div>
</template>
<script setup lang="ts">
import { computed, reactive, ref } from "vue";
const activeItem = ref("Story");
const tabs = reactive([
  {
    title: "Story",
    img: "https://mocossi.com/static/media/group_164@3x.35627a179e2fd89f4bb1.jpg",
    content: `
2038 was a landmark year in technology and production that brought humanity to an unprecedented level of development. Skyscrapers rose, unmanned vehicles filled the streets, factories in industrial zones worked nonstop and cities never slept. Over time, this progress led to a variety of alarming consequences: depletion of natural resources, inability of plants and animals to survive, and increased pollution.`,
  },
  {
    title: "Breeding",
    img: "https://mocossi.com/static/media/group_2474@3x.4a1a8924a4a599ef46fa.jpg",
    content: `
    Mr. X! once discovered that seeds brought back from planet Mocossi grow much faster and stronger than those on Earth. Since then, scientists have been experimenting with resources from this planet. Unfortunately, our size and physical condition limit our ability to fully farm for resources on Mocossi.

Scientists have also confirmed that there exist lovely, plump-body creatures with characteristics that resemble pets on Earth. The first species discovered on planet Mocossi was known as ITO (intelligent & true-blue object) for its intelligence and loyalty. Meanwhile, all creatures on this planet (including yet to be discovered species) are given the common name - Mocomon.

In an ambitious plan devised by scientists, mankind is projected to live peacefully with Mocomons on this planet while keeping Mother Earth from suffering resource shortages or environmental damage.The first step is to develop a breeding program to conduct genetic research and to expand the Mocomon population. At least two ITOs must be involved in breeding. ITOs require a seven-day cooldown period after each breed. An ITO can only breed a maximum of ten times in its lifetime.`,
  },
  {
    title: "Mocossi Planet",
    img: "https://mocossi.com/static/media/group_2478@3x.8024879256698c2a9793.jpg",
    content: `
    The next phase of the plan is to nurture and cultivate Mocomons. To adjust to their new life, they require constant attention from humans concerning basic needs such as feeding, bathing, cleaning and sleeping.

Humans and Mocomons are expected to gradually adapt to each other's existence over time. Mocomons have a variety of survival skills (planting, fishing, and farming) and consequently will be able to perform tasks relevant to their skills.`,
  },
]);
const current = computed(() => {
  return tabs.find((i) => i.title == activeItem.value) || tabs[0];
});
const onChangeTab = (text: string) => {
  activeItem.value = text;
};
</script>
<style module lang="less">
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
    .tabs {
      // display: flex;
      text-align: center;
      z-index: 1;
    }
    .tab-item {
      display: inline-block;
      .tab-item-button {
        background-color: transparent;
        background-repeat: no-repeat;
        background-size: 100% 100%;
        border: 0;
        margin: 0 11px 40px;
        height: 92px;

        background-image: url(https://mocossi.com/static/media/standy.0b24266fec04aac19daf.svg);
        width: 250px;
        cursor: pointer;
        &.active {
          text-shadow: -1px -1px 0 #dc1c98;
          background-image: url(https://mocossi.com/static/media/selected.5ed055d9d3f6f807658e.svg);
        }
        &:hover {
          text-shadow: -1px -1px 0 #dc1c98;
        }
        span {
          color: #fff;
          font-family: iCiel Cadena;
          font-size: 24px;
          font-weight: 900;
          line-height: 24px;
          text-align: center;
        }
      }
    }

    .content {
      height: 620px;
      margin-left: auto;
      margin-right: auto;
      position: relative;
      width: 1102px;
      z-index: 1;

      .img {
        position: absolute;
        top: 0;
        left: 0;
        z-index: 0;
        width: 1102px;
        height: 620px;
        border-radius: 20px;
      }
      .desc {
        border-radius: 20px;
        left: 20px;
        right: 20px;
        bottom: 20px;
        position: absolute;
        // width: 80%;
        height: 110px;

        z-index: 1;
        background-color: rgba(53, 0, 40, 0.9);
        color: #fff;
        padding: 20px;
        p {
          height: 100%;
          overflow-y: auto;
          font-size: 19px;
          font-weight: 700;
          line-height: 25px;
        }
      }
    }
  }
}
</style>
