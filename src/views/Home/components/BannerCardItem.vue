<template>
  <div :class="$style.container">
    <div :class="$style.content">
      <div :class="$style.box">
        <div>
          <img src="@/assets/bg.svg" alt="" :class="$style.bg" />
          <img :src="data.img" alt="" :class="$style.img" />
          <div :class="$style.number">450</div>
        </div>

        <div></div>
      </div>
      <p :class="$style.text">{{ data.text }}</p>
    </div>
  </div>
</template>
<script setup lang="ts">
type ItemType = {
  text: string;
  img: string;
};
defineProps<{ data: ItemType }>();
</script>
<style module lang="less">
.container {
  align-items: center;
  background: linear-gradient(
    180deg,
    rgba(53, 0, 40, 0),
    #350028 48.51%,
    rgba(53, 0, 40, 0)
  );
  display: flex;
  justify-content: center;
  margin: 0 20px;
  transform: all 0.3s;
  &:hover {
    transform: translateY(-10px);
  }
}
.content {
  background: linear-gradient(
    180deg,
    rgba(53, 0, 40, 0),
    #350028 48.51%,
    rgba(53, 0, 40, 0)
  );
  display: flex;
  flex-direction: column;
  margin: 50px 10px;
  padding: 50px 30px;
}
.box {
  display: flex;
  position: relative;
  .bg {
    height: 184px;
    margin-top: 30px;
    width: 154px;
  }
  .img {
    border-radius: 16px;
    height: 142px;
    left: auto;
    left: 50%;
    position: absolute;
    right: auto;
    top: 0;
    top: 6px;
    -webkit-transform: translate(-50%);
    transform: translate(-50%);
    width: 142px;
    z-index: 200;
  }
  .number {
    position: absolute;
    bottom: 40px;
    left: 50%;
    position: absolute;
    -webkit-transform: translate(-50%);
    transform: translate(-50%);
    color: #0033ad;
    font-weight: bold;
  }
}
.text {
  color: #fff;
  font-family: Quicksand;
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 22px;
  margin-top: 20px;
  text-align: center;
}
</style>
