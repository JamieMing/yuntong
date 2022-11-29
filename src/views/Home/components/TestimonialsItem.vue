<template>
  <div :class="$style.container">
    <p>{{ data.text }}</p>
    <div class="user-box">
      <img :src="data.img" alt="" />
      <div>
        <div class="username">{{ data.username }}</div>
        <div class="subText">Twitter</div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
export type ItemType = {
  text: string;
  img: string;
  key?: number;
  username: string;
};
defineProps<{ data: ItemType }>();
</script>
<style lang="less" module>
.container {
  background-image: url(https://mocossi.com/static/media/item.a2bd3d879622ba59e399.svg);
  background-repeat: no-repeat;
  background-size: contain;
  display: flex;
  flex-direction: column;
  height: 477px;
  margin: 10px;
  padding: 50px 30px 30px;
  text-align: left;
  width: 512px;
  :global {
    p {
      color: #fff;
      flex: 1 1;
      font-family: Quicksand;
      font-size: 24px;
      font-style: normal;
      font-weight: 700;
      line-height: 30px;
    }
    .user-box {
      height: 46px;
      display: flex;
      align-items: center;
      img {
        border-radius: 100%;
        height: 64px;
        width: 64px;
        margin-right: 15px;
      }
      .username {
        color: #fff;
        font-family: Quicksand;
        font-size: 18px;
        font-style: normal;
        font-weight: 700;
        line-height: 22px;
        text-align: justify;
      }
      .subText {
        color: #fff;
        font-family: Poppins;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 21px;
        text-align: justify;
      }
    }
  }
}
</style>
