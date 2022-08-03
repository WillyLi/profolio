<template>
  <div class="about">
    <div class="wrap">
      <div class="about-content">
        <div class="about-item">
          <div class="skill">
            <div class="skill-title">Web Development</div>
            <ul>
              <li>HTML</li>
              <li>CSS/SCSS/BEM</li>
              <li>Javascript</li>
              <li>Vue</li>
              <li>JQuery</li>
              <li>GIT</li>
              <li>RWD</li>
            </ul>
          </div>
        </div>
        <div class="about-item">
          <div class="skill">
            <div class="skill-title">Design</div>
            <ul>
              <li>Photoshop</li>
              <li>Illustator</li>
              <li>After Effect</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.about {
  background: #e18822;
  color: #fff;
  font-size: 22px;
  padding: 20px;
  &-content {
    display: flex;
  }
  &-item {
    width: 50%;
  }
}

@media screen and (max-width: 768px) {
  .about {
    &-content {
      display: block;
    }
    &-item {
      width: 100%;
    }
  }
}
</style>
