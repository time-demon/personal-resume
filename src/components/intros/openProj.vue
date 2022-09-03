<!-- 开源项目 -->
<template>
  <div class="introBox">
    <div class="titleBox">
      <p class="line"></p>
      <p class="title">
        <span>开源项目</span>
      </p>
    </div>
    <div class="introCon">
      <div class="projectBox">
        <div class="projectTitle">
          <p class="bold">时光搜题小程序 - 微信小程序</p>
          <p class="projectTitleRight">
            <a href=""><i class="sg sg-gitee-fill-round"></i></a>
            <a href=""><i class="sg sg-github-fill"></i></a>
            <span>|</span>
            <a href="javascript:void (0)" @click="openImg('时光搜题小程序', 'https://img.timebk.cn/时光搜题/时光搜题小程序.jpg')">线上体验</a>
          </p>
        </div>
        <li>答案查询小程序，查题积分制，可结合流量主实现积分奖励</li>
        <li>
          普通功能
          <span class="keyW1">从服务器获取配置</span>、<span class="keyW1">完整的前后端登录流程</span>、 <span
            class="keyW1">自定义查题接口</span>、<span class="keyW1">搜题记录</span>(可删)
        </li>
        <li>
          积分功能
          <span class="keyW1">看广告加积分</span>、<span class="keyW1">查题扣积分</span>
        </li>
        <li>
          额外功能
          <span class="keyW1">抖音无水印解析</span>(需服务器反向代理)、<span class="keyW1">工具箱</span>(可根据模板自行添加)
        </li>
      </div>
    </div>
    <div class="introCon">
      <div class="projectBox">
        <div class="projectTitle">
          <p class="bold">个人简历 - Vue版</p>
          <p class="projectTitleRight">
            <a href=""><i class="sg sg-gitee-fill-round"></i></a>
            <a href=""><i class="sg sg-github-fill"></i></a>
            <span>|</span>
            <a href="javascript:void (0)" @click="openImg('个人简历', 'https://img.timebk.cn/时光搜题/个人简历Vue.png')">线上体验</a>
          </p>
        </div>
        <li>漂亮的原创个人简历Vue源码，提供模块化模板</li>
        <li>没错，就是您当前看到的这个在线简历</li>
        <li>
          额外功能：
          <span class="keyW1">简历PDF下载</span>(有的样式因为依赖本身的问题会不正常)
        </li>
      </div>
    </div>
  </div>
</template>
<!-- npm i element-ui -S -->
<script>
export default {
  methods: {
    openImg(title, img) {
      let _this = this;
      this.$alert(
        `<img src="${img}">`,
        `${title}`,
        {
          dangerouslyUseHTMLString: true,
          center: true,
          showConfirmButton: false
        }
      )
    },
  },
};
</script>

<style lang="scss" scoped>
.introCon {
  padding: 10px 30px;

  >.projectBox {
    >.projectTitle {
      padding: 0 0 10px 0;
      display: flex;
      vertical-align: top;
      justify-content: space-between;
      align-items: center;

      >.projectTitleRight {
        font-size: 13px;

        >a {
          padding-left: 5px;
        }

        >span {
          padding: 0 5px;
          color: #ccc;
        }
      }
    }
  }
}
</style>