<template>
  <div :class="$style.container">
    <img
      src="https://mocossi.com/static/media/group_2460@2x.8701d6bf90e74fbc56e4.jpg"
      alt=""
      class="bg"
    />
    <div class="header">
      <h2>Our Team</h2>
      <h3>
        In early August 2021, we formed a solid team of successful entrepreneurs
        from diverse backgrounds. The caliber of our blockchain engineers,
        talented artists, skilled game developers, marketing and content
        specialists is our hallmark and driving force for us to move forward.
      </h3>
    </div>
    <div class="content">
      <div class="card" v-for="(item, index) in data" :key="index">
        <div class="bg">
          <div class="overlay">
            <div class="inner">
              <img :src="item.img" alt="" class="user-img" />
              <div class="name">{{ item.name }}</div>
              <div class="job">{{ item.job }}</div>
              <img src="@/assets/in.svg" alt="" />
              <div class="hidden">
                <div class="line"></div>
                <div class="desc">{{ item.desc }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive } from "vue";

const data = reactive([
  {
    img: "https://mocossi.com/static/media/mr_lam.43ac39ed9a952d1b6a0ee9196ec6ae30.svg",
    name: "LAM HA",
    job: "Lead Developer",
    social: "in",
    desc: "Game producer.Project manager for several E-commerce and Blockchain projects.",
  },
]);
Array.from({ length: 20 }).map((i) => {
  data.push(data[0]);
});
</script>
<style lang="less" module>
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
      h3 {
        margin-top: 20px;
        color: #ffe81c;
        font-family: Quicksand;
        font-size: 24px;
        font-style: normal;
        font-weight: 700;
        line-height: 30px;
        padding-left: 20px;
        padding-right: 20px;
        text-align: center;
        width: 1200px;
      }
    }

    .content {
      padding: 0 160px;
      z-index: 1;
      display: flex;
      flex-wrap: wrap;
      .card {
        margin: 16px 10px;
        position: relative;
        flex: 0 0 378px;
        height: 318px;
        .bg {
          background-image: url(https://mocossi.com/static/media/member_bg.9d0b5899b6c550a7a772.png);
          background-repeat: no-repeat;
          background-size: 100% 100%;
          height: 100%;
          padding-top: 20px;
          width: 100%;
          .overlay {
            height: 100%;
            overflow: hidden;
            position: relative;
          }
        }
      }
      .card:hover {
        .inner {
          transform: translateY(calc(-100% + 80px));
        }
      }
      .inner {
        display: flex;
        flex-direction: column;
        // justify-content: space-between;
        align-items: center;
        padding: 20px;
        height: 100%;
        color: #fff;
        transition: all 1s;
        position: relative;
        .user-img {
          border-radius: 50%;
          height: 100px;
          width: 100px;
        }
        .name {
          color: #fff;
          font-family: Quicksand;
          font-size: 24px;
          font-style: normal;
          font-weight: 700;
          line-height: 30px;
          margin: 20px 0 10px;
          text-align: center;
        }
        .job {
          color: #ebe9eb;
          font-family: Quicksand;
          font-size: 18px;
          font-style: normal;
          font-weight: 500;
          line-height: 22px;
          margin-bottom: 30px;
        }
      }
      .hidden {
        position: absolute;
        top: 100%;
      }
      .line {
        height: 4px;
        background-color: #fff;
        width: 50px;
        margin: 20px auto;
        // align-items: center;
      }
      .desc {
        padding: 20px;
        color: #ebe9eb;
        font-family: Quicksand;
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 22px;
        opacity: 0.6;
        text-align: center;
      }
    }
  }
}
</style>
