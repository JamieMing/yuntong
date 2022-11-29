<template>
  <div :class="$style.container">
    <div :class="$style.content">
      <div :class="$style.box">
        <div>
          <img :src="data.img" alt="" :class="$style.img" />
        </div>
      </div>
      <p :class="$style.text" v-html="data.text"></p>
    </div>
  </div>
</template>
<script setup lang="ts">
type ItemType = {
  text: string;
  img: string;
  key?: number;
};
defineProps<{ data: ItemType }>();
</script>
<style module lang="less">
.container {
  float: left;
  background: linear-gradient(
    180deg,
    rgba(53, 0, 40, 0),
    #350028 48.51%,
    rgba(53, 0, 40, 0)
  );
  height: 600px;
  margin: 10px;
  padding: 38px 20px;
  width: 100%;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: linear-gradient(
    180deg,
    rgba(53, 0, 40, 0),
    #350028 48.51%,
    rgba(53, 0, 40, 0)
  );
}
.box {
  position: relative;
  .bg {
    height: 184px;
    margin-top: 30px;
    width: 154px;
  }
  .img {
    // border-radius: 16px;
    height: 176px;
    width: 186.81px;
    display: block;
  }
}
.text {
  margin-top: 20px;
  color: #fff;
  font-family: Quicksand;
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  line-height: 40px;
  text-align: center;
  text-transform: uppercase;
}
</style>
