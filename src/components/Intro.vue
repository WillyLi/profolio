<template>
  <div class="intro">
    <div class="wrap">
      <div class="intro-content">
        <div class="profile">
          <div class="basicInfo">
            <div class="basicInfo-image">
              <img src="../assets/profile.jpg" alt="" />
            </div>
            <div class="basicInfo-content">
              <div class="basicInfo-name">CHENG <br />EN<br />LYU</div>
              <ul class="basicInfo-contact">
                <li>
                  <img
                    src="../assets/phone.png"
                    class="basicInfo-icon"
                  />0912345678
                </li>
                <li>
                  <img
                    src="../assets/email.png"
                    class="basicInfo-icon"
                  />abc@gmail.com
                </li>
              </ul>
            </div>
          </div>
          <div class="experience experience--education">
            <div class="experience-title">EDUCATION</div>
            <ul>
              <li>
                <div class="experience-main">能仁家商</div>
                <div class="experience-sub">廣告設計</div>
              </li>
              <li>
                <div class="experience-main">能仁家商</div>
                <div class="experience-sub">廣告設計</div>
              </li>
              <li>
                <div class="experience-main">能仁家商</div>
                <div class="experience-sub">廣告設計</div>
              </li>
            </ul>
          </div>
          <div class="experience experience--work">
            <div class="experience-title">WOKR EXPERIENCE</div>
            <ul>
              <li>
                <div class="experience-main">2018/08 - 2019/08</div>
                <div class="experience-sub">Electronic Commerce Designer</div>
              </li>
              <li>
                <div class="experience-main">2018/08 - 2019/08</div>
                <div class="experience-sub">Electronic Commerce Designer</div>
              </li>
            </ul>
          </div>
        </div>
        <div class="skills">
          <div class="skill">
            <div class="skill-title"><b>W</b>eb</div>
            <ul class="skill-list">
              <li class="skill-item">
                <img src="../assets/html.png" alt="" />
              </li>
              <li class="skill-item">
                <img src="../assets/sass.png" alt="" />
              </li>
              <li class="skill-item">
                <img src="../assets/vue.png" alt="" />
              </li>
            </ul>
          </div>
          <div class="skill">
            <div class="skill-title"><b>D</b>esign</div>
            <ul class="skill-list">
              <li class="skill-item">
                <img src="../assets/html.png" alt="" />
              </li>
              <li class="skill-item">
                <img src="../assets/sass.png" alt="" />
              </li>
              <li class="skill-item">
                <img src="../assets/vue.png" alt="" />
              </li>
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
.intro {
  height: 80vh;
  padding-top: 150px;
  background: #555;
  &-content {
    position: relative;
  }
}
.basicInfo {
  width: 50%;
  display: flex;
  &-image {
    flex-shrink: 0;
    width: 200px;
    height: 200px;
    overflow: hidden;
    border-radius: 50%;
    img {
      width: 100%;
    }
  }
  &-content {
    padding-left: 20px;
  }
  &-name {
    font-size: 50px;
    font-weight: bold;
    line-height: 40px;
  }
  &-icon {
    width: 30px;
    margin-right: 5px;
  }
  &-contact {
    padding: 10px 0;
    margin: 0;
    list-style: none;
    li {
      display: flex;
      align-items: center;
      margin-bottom: 5px;
    }
  }
}
.experience {
  &-title {
    font-weight: bold;
    color: lightblue;
    margin-bottom: 10px;
  }
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: flex;
    margin-bottom: 10px;
  }
  &-main {
    color: white;
    font-size: 20px;
    margin-right: 10px;
  }
  &-sub {
    color: #aaa;
    font-size: 14px;
    background: #000;
    height: 26px;
    line-height: 26px;
    border-radius: 13px;
    padding: 0 10px;
  }
  & + & {
    margin-top: 40px;
  }
}
.profile {
  box-sizing: border-box;
  width: 65%;
  background: #777;
  padding: 50px;
  border-radius: 20px;
  box-shadow: 0 5px 10px #333;
  position: relative;
  z-index: 1;
}
.skills {
  box-sizing: border-box;
  position: absolute;
  width: calc(35% + 30px);
  top: 0;
  left: 65%;
  padding-top: 50px;
  margin-left: -30px;
}
.skill {
  background: #999;
  padding: 20px 50px;
  border-radius: 20px;
  box-shadow: 0 5px 10px #333;
  & + & {
    margin-top: 40px;
  }
  &-title {
    font-size: 20px;
    font-weight: bold;
    b {
      font-size: 40px;
    }
  }
  &-list {
    margin: 0;
    padding: 20px;
    display: flex;
    list-style: none;
  }
  &-item {
    & + & {
      margin-left: 10px;
    }
  }
  img {
    width: 30px;
  }
}

@media screen and (max-width: 768px) {
  .intro {
    height: auto;
    padding-top: 100px;
    padding-bottom: 50px;
  }
  .profile {
    width: 100%;
    padding: 20px;
  }
  .skills {
    position: relative;
    width: 100%;
    top: 0;
    left: 0;
    margin-left: 0;
  }
  .skill {
    padding: 20px;
  }
  .basicInfo {
    &-name {
      font-size: 40px;
      line-height: 30px;
    }
    &-image {
      width: 150px;
      height: 150px;
    }
    &-icon {
      width: 20px;
    }
  }
  .experience {
    &-main {
      font-size: 18px;
    }
    &:last-child li {
      display: block;
    }
  }
}
</style>
