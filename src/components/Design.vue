<template>
  <div class="design">
    <div class="wrap">
      <div class="design-title">Design</div>
    </div>
    <swiper
      class="design-list"
      :slidesPerView="'1'"
      :spaceBetween="10"
      :centeredSlides="true"
      :navigation="true"
      :modules="modules"
      :initialSlide="1"
      :breakpoints="{
        '768': {
          slidesPerView: 2,
          spaceBetween: 20,
        },
      }"
    >
      <swiper-slide
        class="design-item swiper"
        v-for="(item, key) in items"
        :key="key"
      >
        <div class="design-image">
          <img :src="item.url" />
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css";
import "swiper/css/navigation";
import { Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Navigation],
      items: [
        { url: "/src/assets/design1.jpg" },
        { url: "/src/assets/design2.jpg" },
        { url: "/src/assets/design3.jpg" },
        { url: "/src/assets/design4.jpg" },
        { url: "/src/assets/design5.jpg" },
        { url: "/src/assets/design6.jpg" },
        { url: "/src/assets/design7.jpg" },
        { url: "/src/assets/design8.jpg" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.design {
  padding: 50px;
  &-title {
    font-size: 40px;
    margin-bottom: 20px;
  }
  &-item {
    padding: 30px;
    box-sizing: border-box;
    img {
      transition: transform ease 0.2s;
      width: 100%;
    }
  }
}
.swiper-slide-active {
  img {
    transform: scale(1.2);
  }
}
@media screen and (max-width: 768px) {
  .design {
    padding: 40px 20px;
  }
}
</style>
<style>
.swiper-button-next,
.swiper-button-prev {
  color: #222;
  text-shadow: 0 0 3px #fff;
}
</style>
