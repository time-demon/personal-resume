<template>
  <div id="app">
    <router-view></router-view>
    <div class="github">
      <i class="sg sg-github-fill"></i>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
  }
}
</script>

<style lang="scss">
.el-message-box {
  max-width: 100% !important;

  img {
    max-width: 100% !important;
  }
}

.github {
  position: absolute;
  top: 10px;
  right: 10px;

  >i {
    font-size: 30px;
    cursor: pointer;
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
</style>
