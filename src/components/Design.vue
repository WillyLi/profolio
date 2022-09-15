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
import design1 from "@/assets/design1.jpg";
import design2 from "@/assets/design2.jpg";
import design3 from "@/assets/design3.jpg";
import design4 from "@/assets/design4.jpg";
import design5 from "@/assets/design5.jpg";
import design6 from "@/assets/design6.jpg";
import design7 from "@/assets/design7.jpg";
import design8 from "@/assets/design8.jpg";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Navigation],
      items: [
        { url: design1 },
        { url: design2 },
        { url: design3 },
        { url: design4 },
        { url: design5 },
        { url: design6 },
        { url: design7 },
        { url: design8 },
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
