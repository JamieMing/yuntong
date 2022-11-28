<template>
  <div :class="$style.container">
    <div class="header">
      <h2>Encyclopedia</h2>
    </div>

    <div v-for="(data, index) in listData" :key="index">
      <div class="overlay"></div>
      <vue3ScrollSeamless
        :data-list="data"
        :class-options="{
          direction: index == 1 ? 3 : 2,
          limitMoveNum: 6,
          step: 0.5,
        }"
        class="wrap"
      >
        <ul class="ul-item">
          <li class="li-item" v-for="(item, index) in data" :key="index">
            <img :src="item" alt="" />
          </li>
        </ul>
      </vue3ScrollSeamless>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive } from "vue";
import { vue3ScrollSeamless } from "vue3-scroll-seamless";

const listData = reactive([
  [
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/Qmab13nXz3jMXTfgdzeneTZcoggN4a2TQEdLMFj1qE3HXk",
  ],
  [
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmeDTsgULXDBTs9NzTtfKkjEKkYcAfo9UjPqGwqempsyvf",
  ],
  [
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmfKz1JgaF5RNJQJe4cV6roKfMh6nESE6Sfod5X9ZGZjFv",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmfKz1JgaF5RNJQJe4cV6roKfMh6nESE6Sfod5X9ZGZjFv",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmfKz1JgaF5RNJQJe4cV6roKfMh6nESE6Sfod5X9ZGZjFv",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmfKz1JgaF5RNJQJe4cV6roKfMh6nESE6Sfod5X9ZGZjFv",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmfKz1JgaF5RNJQJe4cV6roKfMh6nESE6Sfod5X9ZGZjFv",
    "https://images.mocossiplanet.com/tr:w-300,q-100,pr…ue/QmfKz1JgaF5RNJQJe4cV6roKfMh6nESE6Sfod5X9ZGZjFv",
  ],
]);
</script>
<style lang="less" module>
:root {
  --gradient-color: rgba(53, 0, 40, 1), rgba(53, 0, 40, 0);
  --gradient-width: 300px;
}
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
    .overlay {
      position: absolute;
      width: 100%;
      height: 100%;
      &::before {
        background: linear-gradient(to right, var(--gradient-color));
        content: "";
        height: 100%;
        position: absolute;
        width: var(--gradient-width);
        z-index: 2;
      }
      &::after {
        right: 0;
        top: 0;
        transform: rotateZ(180deg);
        background: linear-gradient(to right, var(--gradient-color));
        content: "";
        height: 100%;
        position: absolute;
        width: var(--gradient-width);
        z-index: 2;
      }
    }
    .wrap {
      width: var(--global-width);
      z-index: 1;
      overflow: hidden;
      margin-bottom: 20px;
      .ul-item {
        display: flex;
        margin: 0;
        padding: 0;
        .li-item {
          //   width: 220px;
          margin-left: 20px;
          padding: 0;
          text-decoration: none;

          img {
            display: block;
            height: 214px;
            margin: 5px;
            width: 214px;
            border-radius: 14px;
          }
        }
      }
    }
  }
}
</style>
