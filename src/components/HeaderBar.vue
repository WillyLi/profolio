<template>
  <header class="header">
    <div class="wrap">
      <div class="header-content" v-scroll-spy-active v-scroll-spy-link>
        <a class="header-item">About</a>
        <a class="header-item">Showcase</a>
        <a class="header-item">Contact</a>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
  position: fixed;
  top: 0;
  width: 100%;
  background: #e18822;
  z-index: 10;
  &-content {
    display: flex;
  }
  &-item {
    color: #fff;
    text-decoration: none;
    font-size: 24px;
    padding: 0 10px;
    height: 50px;
    line-height: 50px;
    display: block;
    cursor: pointer;
    &.active {
      background-color: #fff;
      color: #e18822;
    }
  }
}
</style>
