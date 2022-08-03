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
  height: 500px;
  background-image: url("../assets/intro.png");
  background-size: cover;
  &-content {
    height: 500px;
    display: flex;
    align-items: center;
  }
  &-text {
    color: white;
    font-size: 40px;
  }
}
@media screen and (max-width: 800px) {
  .intro {
    background-image: url("../assets/intro-m.png");
  }
}
</style>
