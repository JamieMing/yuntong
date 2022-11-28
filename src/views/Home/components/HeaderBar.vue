<template>
  <div class="container">
    <img
      src="https://mocossi.com/static/media/mocossi-icon-header.40813c5a8d3a0e81530c.png"
      alt=""
      class="logo"
    />
    <nav class="nav">
      <a
        :href="item.link"
        v-for="item in datas"
        :key="item.text"
        :class="['nav_item', currentItem == item.text ? 'active' : '']"
        @click="
          (e) => {
            onClick(item.text);
          }
        "
      >
        <div class="nav_indicator" v-show="currentItem == item.text">
          <img src="@/assets/images/nav_active_top.png" alt="" />
          <img src="@/assets/images/nav_active_bottom.png" alt="" />
        </div>
        {{ item.text }}
      </a>
    </nav>
    <div class="user">
      <img
        src="	https://mocossi.com/static/media/notification-icon.71a4f7f042fc68eb72592efbb0e176a4.svg"
        alt=""
      />
      <div class="button">
        <button>Connect Wallet</button>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive, ref } from "vue";
const currentItem = ref("Home");
const datas = reactive([
  {
    link: "#",
    text: "Home",
  },
  {
    link: "#",
    text: "Whitepaper",
  },
  {
    link: "#",
    text: "News",
  },
  {
    link: "#",
    text: "Encyclopedia",
  },
  {
    link: "#",
    text: "Breeding",
  },
  {
    link: "#",
    text: "Land",
  },
  {
    link: "#",
    text: "Airdrop",
  },
  {
    link: "#",
    text: "Marketplace",
  },
]);
const onClick = (text: string) => {
  currentItem.value = text;
};
</script>
<style lang="less" scoped>
.container {
  align-items: center;
  background: #3c2336;
  display: flex;
  height: 80px;
  left: 0;
  padding: 0 40px;
  position: absolute;
  right: 0;
  top: 0;
  z-index: 100;
  .logo {
    height: 64px;
  }
  .nav {
    flex: 1;
    display: flex;
    justify-content: center;
    overflow-x: hidden;
    position: relative;
    .nav_item {
      align-items: center;
      color: #fff;
      display: flex;
      font-family: iCiel Cadena;
      font-weight: 900;
      font-size: 24px;
      // width: 120px;
      height: 80px;
      line-height: 33px;
      position: relative;
      text-decoration: none;
      cursor: pointer;
      &.active {
        text-shadow: 2px 0 0 #dc1c98, -2px 0 0 #dc1c98, 0 2px 0 #dc1c98,
          0 -2px 0 #dc1c98, 1px 1px #dc1c98, -1px -1px 0 #dc1c98,
          1px -1px 0 #dc1c98, -1px 1px 0 #dc1c98, 0 0 20px #dc1c98;
      }
      &:not(:first-child) {
        margin-left: 77px;
      }
      &:hover {
        .active;
      }
    }
    .nav_indicator {
      bottom: 0;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      left: 50%;
      position: absolute;
      top: 0;
      transform: translateX(-50%);
      img {
        display: block;
        width: 108px;
      }
    }
  }
  .user {
    // width: 220px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    img {
      height: 48px;
      margin-left: auto;
      width: 48px;
    }
    .button {
      background-color: #ffbebe;
      border-radius: 8px;
      display: inline-block;
      margin-left: 20px;
      button {
        &:hover {
          box-shadow: 0 0 10px #dc1c98, 0 2px 0 #ffbebe;
        }
        cursor: pointer;
        align-items: center;
        border-radius: 8px;
        color: #fff;
        display: flex;
        font-family: iCiel Cadena;
        font-size: 14px;
        font-weight: 900;
        height: 40px;
        justify-content: center;
        line-height: 19px;
        overflow: hidden;
        padding: 0 16px;
        text-overflow: ellipsis;
        transform: translateY(-2px);
        white-space: nowrap;
        background: #f65f70;
        border: 1px solid #ba2673;
        text-shadow: -2px -2px 0 #ba2673, -2px -1px 0 #ba2673, -2px 0 0 #ba2673,
          -2px 1px 0 #ba2673, -2px 2px 0 #ba2673, -1px -2px 0 #ba2673,
          -1px -1px 0 #ba2673, -1px 0 0 #ba2673, -1px 1px 0 #ba2673,
          -1px 2px 0 #ba2673, 0 -2px 0 #ba2673, 0 -1px 0 #ba2673, 0 0 0 #ba2673,
          0 1px 0 #ba2673, 0 2px 0 #ba2673, 1px -2px 0 #ba2673,
          1px -1px 0 #ba2673, 1px 0 0 #ba2673, 1px 1px 0 #ba2673,
          1px 2px 0 #ba2673, 2px -2px 0 #ba2673, 2px -1px 0 #ba2673,
          2px 0 0 #ba2673, 2px 1px 0 #ba2673, 2px 2px 0 #ba2673;
      }
    }
  }
}
</style>
