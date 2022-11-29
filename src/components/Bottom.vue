<template>
  <div :class="$style.container">
    <div class="content">
      <div class="menu">
        <img
          src="https://mocossi.com/static/media/logo.f218a3ced97449dcf92fc6d1769d0aac.svg"
          alt=""
        />
        <div class="list">
          <p v-for="item in menuList" :key="item.title">{{ item.title }}</p>
        </div>
      </div>
      <div class="contact">
        <p>Join Our Community</p>
        <div class="wrap">
          <img
            alt=""
            src="https://mocossi.com/static/media/discord.01cf86cb1faa581abafa102df65485d5.svg"
          /><img
            alt=""
            src="https://mocossi.com/static/media/tw.e928a7e6859ddb97b98e6487a635e574.svg"
          /><img
            alt=""
            src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHgAAAB4CAMAAAAOusbgAAABUFBMVEUAAAD/AwP/AAD/AAD/AAD/AQH/CAj9Fxf/wcH/AgL/CQn/CQn/Dg7/AwP/Cwv+IiL/BAT/CAj/Bwf/BAT/CAj/DQ3/AwP/ExPyg4P/AQH/Bgb/AgL/AAD/BAT/BQX/CQn/AgL/BQX/CQn/CAj/BAT/AAD/DAz/Dw//AQH+EhL+Fhb/HBz9Hx//fX3/BAT/BAT/Bgb+Cgr/Bgb+DAz/Cwv/Dw//ERH/Fxf/HR3/YGD/YWH/AwP/AgL/AQH/Dg7/DAz+EhL/ERH/ERH/SEj/AAD/Bwf+CAj/Cwv+Cwv/CQn/BQX/EBD/DQ3/AAD/////VFT/ERH/7u7/4OD/ICD//Pz/zs7/r6//hIT/amr/S0v/BAT/8fH/2Nj/v7//urr/oqL/lZX/iIj/fHz/X1//QkL/PDz/JSX/Ghr/Cgr/+Pj/5eX/qKj/f3//fn7/NDT/Ly9iW1wpAAAATXRSTlMA5/37fHpXGwL3Qjkh2G4X8sqkeHZsW00G+evh3dLCu5yYj2VfXFVHPDYyLy0JzbCUjIR0aFJLKCcOC/Tu2rVxUEAeEQ6qiG9iRZ58U7uK3ggAAANNSURBVGje7drXUttAGIbhlYvcbdwbxTbGld57Sy8fNgkhhZJAgJB+/2fJSOP8QBhGq7WXk31u4B2PZnd/r8QURVEURVGUK7xjDzzBhUagVk3P6any8GwyvDGTiLvdLpfLHU8kZp4kZ4fLKX0uXfXX6s2F7ciy124qsrClz8YfFx8NhrQVJ7g5sqv56Hqh5NpIVQPbGSvN0XBhKO9DVzly0Ynp+bG7qlMaesY3obPbPZx2orfGm1QjwTx6zuH+v+tfhQylm92mBjmmr3cf9EMW/7XwFKRZfchI0Al5XIyUIJFGPzkTgkxPaSlBquesIwGpQqxjAlI5ljvhccjVZCZvFnLNMJMHkhWYaQuSDTFTGJL1M9MkJOuj1STZkhkeBIc2uiBohgfAoXXYgrC6Gc6BQ2tn5+NrCEqbYQcsoPBfp20IKRvdJVhE4Z1X7yAizLFxUdj05hz2mVPuKKyjsNCjnjLCAfCg8M7ejw+wp8gzf1CYvPoMW2JGeB4WUZgcX4ATnRIVWEZh8ukLuEWN8AiI9TDZfQtea0Z4GIQjLPKoNSOcBOELk32+pZUzwjMgvGHytg0Dx4Ech0EkbO6i1le1zwi7AZEwefMeXGEXBMPku8VH7exyeO+kzROOdyu8/xsW+egvm3j48AwAV3gDgHB49x049IlvILSKeeS6tGUenYOP1pVD4lsLvEJGWAfhDx+cfgAXOhbTILzhPTqNeayLjj5HZ+BGo08DHK6Gd9/DpkkjvAgOFP768xJ2PRYY6PcvYA8N9Mvg0aIT0L4kM2RhCYV3WxCjm2ENFlD44KQNQc/McAgcWse/ICxg4yriEqLoKiIG2cbu+bopDMkGmKkOqehKMQLJiszk7YNU9FJiAHI1OuECpHJ6O+EnkGqcddQdkKl4Xy+8Ntk/Lki0tkThiA/yhNkVLyBN/9jVcCYKSZxNdk2wH1I4EuyGBdGy7c8iPBI2zpU5RkhSQ2/FIux2nuHBLHrEkZ8MsDtktlyxwZAPXeTUxh+Vyh5myXIw8KwyG58uFdaja1pfliu0kssPDMWKU+5weS6wGPGKfky2vTjaqNdq/up8erNS0VOpkZGRlK5XXm6m56v+WqAxuhj0RJYyXqYoiqIoiqJc8wdNClAB/pQzoAAAAABJRU5ErkJggg=="
          /><img
            alt=""
            src="data:image/png;base64,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"
          /><img
            alt=""
            src="data:image/png;base64,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"
          />
        </div>
      </div>
    </div>
    <div class="copyright">Copyright © 2022. Mocossi. All rights reserved.</div>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const menuList = reactive([
  {
    title: "Home",
    link: "#",
  },
  {
    title: "Breeding",
    link: "#",
  },
  {
    title: "Whitepaper",
    link: "#",
  },
  {
    title: "Home",
    link: "#",
  },
  {
    title: "Breeding",
    link: "#",
  },
  {
    title: "Whitepaper",
    link: "#",
  },
  {
    title: "Home",
    link: "#",
  },
  {
    title: "Breeding",
    link: "#",
  },
  {
    title: "Whitepaper",
    link: "#",
  },
]);
</script>

<style module lang="less">
.container {
  background: #350028;
  display: flex;
  flex-direction: column;
  :global {
    .content {
      background: #392435;
      display: flex;
      flex: 1 1;
      flex-direction: row;
      justify-content: space-between;
      padding: 60px 108px;
      .menu {
        display: flex;
        flex-direction: row;
        img {
          height: 117px;
          margin-right: 129px;
          width: 210px;
        }
      }
      .list {
        display: flex;
        flex-wrap: wrap;
        width: 662px;

        p {
          width: 220px;
          cursor: pointer;
          color: #fff;
          font-family: Quicksand;
          font-size: 18px;
          font-style: normal;
          font-weight: 700;
          line-height: 22px;
          margin-bottom: 19px;
          text-decoration: none;
          white-space: nowrap;
        }
      }
    }
    .contact {
      p {
        color: #fff;
        font-family: Quicksand;
        font-size: 18px;
        font-style: normal;
        font-weight: 700;
        line-height: 22px;
        margin-bottom: 19px;
        text-decoration: none;
        white-space: nowrap;
      }
    }
    .wrap {
      display: flex;

      img {
        width: 40px;
        cursor: pointer;
        margin-left: 20px;
        &:first-of-type {
          margin-left: 0;
        }
      }
    }
    .copyright {
      color: #fff;
      font-family: Quicksand;
      font-size: 14px;
      font-style: normal;
      font-weight: 700;
      line-height: 17px;
      mix-blend-mode: normal;
      opacity: 0.5;
      padding: 20px;
      text-align: center;
    }
  }
}
</style>
