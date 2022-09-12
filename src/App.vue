<template>
  <main class="main">
    <HeaderBar />
    <div v-scroll-spy="{ offset: 50 }">
      <Intro />
      <Showcase />
      <Design />
    </div>
    <footer class="footer">
      <div class="wrap">
        <ul class="contact">
          <li>
            <img src="./assets/phone.png" class="contact-icon" />0912345678
          </li>
          <li>
            <img src="./assets/email.png" class="contact-icon" />abc@gmail.com
          </li>
        </ul>
      </div>
    </footer>
  </main>
</template>

<script>
import HeaderBar from "./components/HeaderBar.vue";
import Intro from "./components/Intro.vue";
import Showcase from "./components/Showcase.vue";
import Design from "./components/Design.vue";

export default {
  components: { HeaderBar, Intro, Showcase, Design },
};
</script>

<style lang="scss" scoped>
.footer {
  background: #aaa;
  padding: 10px 0;
}
.contact {
  display: flex;
  padding: 10px 0;
  margin: 0;
  list-style: none;
  li {
    display: flex;
    align-items: center;
    margin-right: 10px;
  }
  &-icon {
    width: 30px;
    margin-right: 5px;
  }
}
</style>
