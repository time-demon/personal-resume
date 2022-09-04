<template>
  <div id="app">

    <div class="copyright">
      <span v-html="$store.state.v"></span>
    </div>

    <router-view></router-view>

    <div class="github">
      <a target="_blank" href="https://github.com/time-demon"><i class="sg sg-github-fill"></i></a>
    </div>

  </div>
</template>

<style lang="scss">
.copyright {
  z-index: 999999999999999999;
  cursor: context-menu;
  pointer-events: none;
  font-size: 12px;
  text-align: right;
  padding: 0 5px;
  color: #aaa;
  position: fixed;
  top: 2px;
  right: 2px;
  text-shadow: 1px 1px 0px #fff;
}

.el-message-box {
  max-width: 100% !important;

  img {
    max-width: 100% !important;
  }
}

.github {
  position: absolute;
  top: 18px;
  right: 18px;

  >a {
    text-decoration: none !important;

    >i {
      font-size: 30px;
      cursor: pointer;
    }
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #777;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background: #eee;
}

a {
  text-decoration: none;
  color: inherit;
}

a:hover {
  text-decoration: revert;
  opacity: 0.8;
}

li {
  color: #777;
  font-size: 14px;
  line-height: 30px;
}

::-webkit-scrollbar {
  width: 6px;
  /*对垂直流动条有效*/
  height: 6px;
  /*对水平流动条有效*/
}

/*定义滚动条的轨道颜色、内阴影及圆角*/
::-webkit-scrollbar-track {
  border-radius: 4px;
  /* -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3); */
  /* background-color: rosybrown; */
}

/*定义滑块颜色、内阴影及圆角*/
::-webkit-scrollbar-thumb {
  border-radius: 8px;
  background-color: #959aa1;
  /* -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3); */
}

/*定义滑块悬停变化颜色、内阴影及圆角*/
::-webkit-scrollbar-thumb:hover {
  background-color: #467f8d;
}
</style>
