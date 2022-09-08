<template>
  <div class="showcase">
    <div class="wrap">
      <div class="showcase-select">
        <a
          v-for="tab in tabs"
          :key="tab"
          :class="{ active: currentTab === tab }"
          @click="currentTab = tab"
          >{{ tab }}</a
        >
      </div>
      <div class="showcase-content">
        <component :is="currentTab" />
      </div>
    </div>
  </div>
</template>

<script>
import CSS from "./showcases/CSS.vue";
import Timer from "./showcases/Timer.vue";
import Burger from "./showcases/Burger.vue";
import Draw from "./showcases/Draw.vue";
import FAQ from "./showcases/FAQ.vue";
import API from "./showcases/API.vue";

// 列表渲染 + 動態組件
export default {
  components: { CSS, Timer, Burger, Draw, FAQ, API },
  data() {
    return {
      tabs: ["API", "CSS", "Timer", "Burger", "Draw", "FAQ"],
      currentTab: "API",
    };
  },
};
</script>

<style lang="scss" scoped>
.showcase {
  background: #333;
  padding: 30px 0;
  &-content {
    height: 600px;
    background-color: #e18822;
  }
  &-select {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    a {
      cursor: pointer;
      display: block;
      text-decoration: none;
      color: #e18822;
      border: 1px solid #ffc88a;
      color: #fff;
      min-width: 100px;
      font-size: 18px;
      text-align: center;
      transition: background-color 0.3s ease;
      height: 40px;
      line-height: 38px;
      border-radius: 20px;
      box-sizing: border-box;
    }
    .active {
      background-color: #e18822;
    }
  }
}
@media screen and (max-width: 768px) {
  .showcase {
    &-select {
      a {
        height: 30px;
        line-height: 28px;
        border-radius: 15px;
        min-width: 50px;
        font-size: 12px;
      }
    }
  }
}
</style>
