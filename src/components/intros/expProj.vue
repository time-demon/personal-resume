<!-- 项目经历 -->
<template>
  <div class="introBox">
    <div class="titleBox">
      <p class="line"></p>
      <p class="title">
        <span>项目经历</span>
      </p>
    </div>
    <div class="introCon">
      <div class="projectBox">
        <div class="projectTitle">
          <p class="bold"></p>
        </div>
        <li></li>
      </div>
    </div>
  </div>
</template>
<!-- npm i element-ui -S -->
<script>
export default {
  methods: {
    open() {
      this.$alert(
        "<img src='https://img.timebk.cn/时光搜题/时光搜题小程序.jpg'>",
        "微信扫码使用",
        {
          dangerouslyUseHTMLString: true,
          center: true,
          showConfirmButton: false,
        }
      );
    },
  },
};
</script>

<style lang="scss" scoped>
.introCon {
  padding: 0 30px;
  > .projectBox {
    > .projectTitle {
      padding: 0 0 10px 0;
      display: flex;
      vertical-align: top;
      justify-content: space-between;
      align-items: center;
      > .projectTitleRight {
        font-size: 13px;
        > span {
          padding: 0 5px;
          color: #ccc;
        }
      }
    }
  }
}
</style>