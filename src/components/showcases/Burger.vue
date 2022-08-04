<template>
  <div class="burger">
    <div class="frame">
      <div class="center">
        <div :class="menuClass" @click="onClick()">
          <div class="line line-1"></div>
          <div class="line line-2"></div>
          <div class="line line-3"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isClicked: false,
      active: false,
    };
  },
  computed: {
    menuClass() {
      return {
        menu: true,
        noAnimation: !this.isClicked,
        active: this.active,
      };
    },
  },
  methods: {
    onClick() {
      this.isClicked = true;
      this.active = !this.active;
    },
  },
};
</script>

<style lang="scss" scoped>
@import url(https://fonts.googleapis.com/css?family=Open+Sans:700,300);
.burger {
  height: 600px;
  position: relative;
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
  background: #3faf82;
  font-family: "Open Sans", Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.menu {
  width: 50px;
  height: 50px;
  position: relative;
}
.menu:hover {
  cursor: pointer;
}
.line {
  width: 50px;
  height: 8px;
  background: #fff;
  position: absolute;
  border-radius: 3px;
  box-shadow: 0 0 10px #333;
}
.line-1 {
  top: 0;
  left: 0;
  animation: close1 0.5s forwards;
}
.active .line-1 {
  animation: open1 0.5s forwards;
}
.line-2 {
  top: 21px;
  left: 0;
  animation: close2 0.5s forwards;
}
.active .line-2 {
  animation: open2 0.5s forwards;
}

.line-3 {
  top: 42px;
  left: 0;
  animation: close3 0.5s forwards;
}
.active .line-3 {
  animation: open3 0.5s forwards;
}
.noAnimation .line-1,
.noAnimation .line-2,
.noAnimation .line-3 {
  animation: none;
}

@keyframes open1 {
  0% {
    top: 0;
    transform: rotate(0);
  }
  50% {
    top: 21px;
    transform: rotate(0);
  }
  100% {
    top: 21px;
    transform: rotate(-45deg);
  }
}
@keyframes open2 {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(0);
  }
}

@keyframes open3 {
  0% {
    top: 42px;
    transform: rotate(0);
  }
  50% {
    top: 21px;
    transform: rotate(0);
  }
  100% {
    top: 21px;
    transform: rotate(45deg);
  }
}

@keyframes close1 {
  0% {
    top: 21px;
    transform: rotate(-45deg);
  }
  50% {
    top: 21px;
    transform: rotate(0);
  }
  100% {
    top: 0;
    transform: rotate(0);
  }
}
@keyframes close2 {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes close3 {
  0% {
    top: 21px;
    transform: rotate(45deg);
  }
  50% {
    top: 21px;
    transform: rotate(0);
  }
  100% {
    top: 42px;
    transform: rotate(0);
  }
}
</style>
