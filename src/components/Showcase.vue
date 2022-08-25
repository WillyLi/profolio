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
    a {
      cursor: pointer;
      display: block;
      text-decoration: none;
      color: #e18822;
      background-color: #ffc88a;
      color: #fff;
      padding: 10px 0;
      min-width: 100px;
      font-size: 24px;
      text-align: center;
      transition: background-color 0.3s ease;
    }
    .active {
      background-color: #e18822;
    }
  }
}
</style>
