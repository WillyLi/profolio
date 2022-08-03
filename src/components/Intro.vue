<template>
  <div class="intro">
    <div class="wrap">
      <div class="intro-content">
        <div class="intro-text">Hi, I'm Finn.</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.intro {
  height: 60vh;
  background-image: url("../assets/intro.png");
  background-size: cover;
  background-position: right center;
  &-content {
    height: 60vh;
    display: flex;
    align-items: center;
  }
  &-text {
    color: white;
    font-size: 80px;
  }
}
@media screen and (max-width: 768px) {
  .intro {
    background-image: url("../assets/intro-m.png");
    height: 80vh;
    &-content {
      align-items: flex-start;
      justify-content: center;
      padding-top: 50px;
      height: 80vh;
      text-align: center;
    }
    &-text {
      font-size: 40px;
    }
  }
}
</style>
