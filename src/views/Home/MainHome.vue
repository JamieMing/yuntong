<template>
  <div class="global-container">
    <HeaderBar />
    <section class="main">
      <Banner />
      <StoryAndGameplay />
      <Encyclopedia />
      <RoadMap />
      <Testimonials />
      <OurTeam />
      <Bottom />
    </section>
  </div>
</template>

<script setup lang="ts">
import Bottom from "@/components/Bottom.vue";
import { onMounted } from "vue";
import Banner from "./components/Banner.vue";
import Encyclopedia from "./components/Encyclopedia.vue";
import HeaderBar from "./components/HeaderBar.vue";
import OurTeam from "./components/OurTeam.vue";
import RoadMap from "./components/RoadMap.vue";
import StoryAndGameplay from "./components/StoryAndGameplay.vue";
import Testimonials from "./components/Testimonials.vue";
const onChange = () => {
  const dom: any = document.getElementsByTagName("html")[0];
  dom.style = "--innerWidth:" + window.innerWidth + ";";
};

onMounted(() => {
  onChange();
  window.onresize = onChange;
});
</script>
<style scoped>
.global-container {
  width: 1920px;
  transform-origin: left top;
  /* background-color: #000; */
  transform: scale(calc(var(--innerWidth, 1920) / 1920));
  max-height: 100vh;
}
.main {
  margin-top: 80px;
}
</style>
