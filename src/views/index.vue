<template>
  <div :class="$store.state.isMobile ? 'pageBox pageBox_mobile' : 'pageBox'">

    <!-- 简历 -->
    <div class="cartBox" id="print" v-loading="loading" element-loading-text="准备下载PDF"
      element-loading-spinner="el-icon-loading">
      <myInforBox :myiInfo="myiInfo" />
      <myIntroBox :myiInfo="myiInfo" />
    </div>
    <!-- 简历 -->

    <!-- 右下角 -->
    <div class="sideBox">
      <div class="sideTool" @click="pdfDown">
        <i class="sg sg-pdf"></i>
      </div>
    </div>
    <!-- 右下角 -->

    <!-- 底部 -->
    <div class="footer">
      如果您想了解更多关于我，请
      <a href="javascript:void(0)" @click="QQopen">点击此处</a> 或访问
      <a target="_blank" :href="myiInfo.blog">我的博客</a>
    </div>
    <!-- 底部 -->

  </div>
</template>

<script>
import myInforBox from "@/components/myInforBox.vue";
import myIntroBox from "@/components/myIntroBox.vue";
import htmlToPdf from "@/common/htmlToPdf.js";
export default {
  components: {
    myInforBox,
    myIntroBox,
  },
  data() {
    return {
      myiInfo: {
        name: '何贵江',
        nameEn: 'Guijiang He',
        gender: '男',
        jobWant: 'Web前端开发',
        moneyWant: '7k',
        edu: '专科',
        address: '四川成都',
        phone: 15196923235,
        email: '1937966358@qq.com',
        blog: 'https://timebk.cn/',
        github: 'https://github.com/time-demon',
        gitee: 'https://gitee.com/time-demon',
        csdn: 'https://blog.csdn.net/qq_19322833',
        juejin: 'https://juejin.cn/user/770072696587341',
      },
      display: "grid",
      clientWidth: document.documentElement.clientWidth,
      loading: false
    }
  },
  watch: {

    // 动态监听窗口尺寸
    clientWidth(val) {
      if (val < 840) {
        this.display = 'block';
        this.$store.state.isMobile = true;
      } else {
        this.display = 'grid';
        this.$store.state.isMobile = false;
      }
    },

  },
  created() {
    document.title = this.myiInfo.name + ' - 我的个人简历'
  },
  mounted() {

    // 挂载后获取窗口尺寸
    window.onresize = () => {
      return (() => {
        window.clientWidth = document.documentElement.clientWidth
        this.clientWidth = document.documentElement.clientWidth
      })()
    }
    if (this.clientWidth < 840) {
      this.display = 'block';
      this.$store.state.isMobile = true;
    } else {
      this.display = 'grid';
      this.$store.state.isMobile = false;
    };

  },
  methods: {

    // 下载简历为PDF
    pdfDown() {
      htmlToPdf.downloadPDF("resultOriginal", "个人简历 - 何贵江");
      this.loading = true
      setTimeout(() => {
        this.loading = false
        this.$message({
          message: '成功下载',
          type: 'success'
        });
      }, 1000)
    },

    // 打开联系我QQ弹窗
    QQopen() {
      this.$alert(
        "<img src='https://img.timebk.cn/时光搜题/手机QQ扫码加好友.png'>",
        "QQ扫码添加我",
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

<style lang="scss">
.pageBox {
  max-width: 1024px;
  margin: auto;
  padding: 60px 0 0 0;

  >.sideBox {
    position: fixed;
    z-index: 1;
    right: 20px;
    bottom: 20px;

    >.sideTool {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: rgb(183, 172, 172);
      margin-top: 10px;
      display: flex;
      vertical-align: top;
      justify-content: center;
      align-items: center;
      color: #fff;
      cursor: pointer;

      >i {
        font-size: 25px;
      }
    }

    >.sideTool:hover {
      opacity: .8;
    }
  }

  >.cartBox {
    box-shadow: 0 0 5px #ccc;
    border-radius: 10px;

    >.myInforBox {
      border-radius: 10px 10px 0 0;
      color: #fff;
      background: linear-gradient(90deg, #00c9b8 0%, #00bdc4 100%);
      padding: 10px 50px;
    }

    >.myIntroBox {
      background: #fff;
      border-radius: 0 0 10px 10px;
      padding: 0 15px 15px;
      display: grid;
      grid-template-columns: repeat(2, 50%);
      justify-content: space-between;

      .introBox {
        height: max-content;

        >.titleBox {
          height: 30px;
          position: relative;
          margin: 0 0 15px 0;

          >.line {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            border-bottom: 1px solid #ededed;
            width: 100%;
          }

          >.title {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background: #fff;
            padding: 0 15px;

            >span {
              background: #f5f5f5;
              padding: 5px 20px;
              border-radius: 50px;
            }
          }
        }
      }
    }
  }

  >.footer {
    text-align: center;
    margin: 20px 0;
    padding: 0 5px;

    a {
      text-decoration: underline;
    }
  }
}

.pageBox_mobile {
  padding: 0;

  >.cartBox {
    border-radius: 0;

    >.myInforBox {
      border-radius: 0;
      padding: 10px 15px;
    }

    >.myIntroBox {
      border-radius: 0;
      display: block;
      padding: 0;

      .introBox:nth-of-type(1) {
        padding: 20px 0 10px;
      }

      .introBox {
        padding: 10px 0 10px;
      }
    }
  }

  >.moreBox {
    font-size: 12px;
  }

  >.footer {
    font-size: 14px;
  }
}

.downImgButoon {
  background: #409eff;
  color: #fff;
  padding: 10px 15px;
  border-radius: 4px;
  cursor: pointer;
}

.downImgButoon:hover {
  opacity: .8;
}
</style>