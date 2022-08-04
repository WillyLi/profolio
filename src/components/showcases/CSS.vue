<template>
  <div class="cssChanllenge">
    <div class="frame">
      <div class="center">
        <div class="hundred">
          <div class="one">
            <div class="one-head"></div>
            <div class="one-tail"></div>
          </div>
          <div class="zero zero-one"></div>
          <div class="zero zero-two"></div>
        </div>
        <div class="days">DAYS</div>
        <div class="css">CSS CHALLENGE</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import url(https://fonts.googleapis.com/css?family=Open+Sans:700,300);
.cssChanllenge {
  position: relative;
  height: 600px;
}
.frame {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 400px;
  margin-top: -200px;
  margin-left: -200px;
  border-radius: 2px;
  box-shadow: 4px 8px 16px 0 rgba(0, 0, 0, 0.1);
  overflow: hidden;
  background: #fff;
  color: #333;
  font-family: "Courier New", "Courier", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* Permalink - use to edit and share this gradient: https://colorzilla.com/gradient-editor/#43389f+0,43389f+0,4ec6ca+100 */
  background: rgb(67, 56, 159); /* Old browsers */
  background: -moz-linear-gradient(
    45deg,
    rgba(67, 56, 159, 1) 0%,
    rgba(67, 56, 159, 1) 0%,
    rgba(78, 198, 202, 1) 100%
  ); /* FF3.6-15 */
  background: -webkit-linear-gradient(
    45deg,
    rgba(67, 56, 159, 1) 0%,
    rgba(78, 198, 202, 1) 100%
  ); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(
    45deg,
    rgba(67, 56, 159, 1) 0%,
    rgba(78, 198, 202, 1) 100%
  ); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#43389f', endColorstr='#4ec6ca',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */
  color: #fff;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%); //shift 位移
}

.hundred {
  display: flex;
}
.days {
  text-align: center;
  font-size: 82px;
  line-height: 60px;
  font-weight: 700;
}
.css {
  text-align: center;
  font-size: 23px;
  line-height: 20px;
  font-weight: 700;
  letter-spacing: 0.04em;
}

.one {
  position: relative;
}

.one-tail {
  height: 100px;
  width: 24px;
  background: #fff;
  box-shadow: 0 0 13px 0 rgba(0, 0, 0, 0.2);
  border-radius: 5px;
  position: relative;
  z-index: 3;
}
.one-head {
  content: "";
  height: 40px;
  width: 20px;
  background: #fff;
  display: block;
  border-radius: 5px;
  transform: translate(-15px, 0px) rotate(50deg);
  box-shadow: 0 0 13px 0 rgba(0, 0, 0, 0.2);
  position: absolute;
  z-index: 1;
}

.zero {
  height: 100px;
  width: 100px;
  border-radius: 50%;
  box-shadow: 0 0 13px 0 rgba(0, 0, 0, 0.2);
  border: 24px solid #fff;
  box-sizing: border-box;
  margin-left: -17px;
  position: relative;
}
.zero-one {
  z-index: 2;
}
.zero-two {
  z-index: 1;
}
</style>
