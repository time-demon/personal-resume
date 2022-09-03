<template>
  <div :class="$store.state.isMobile ? 'myInforBox myInforBox_mobile' : 'myInforBox'">
    <div class="topBox">
      <div class="leftBox">
        <span class="nameCn">何贵江</span>
        <span class="nameEn">Guijiang He</span>
      </div>
      <div class="rightBox">
        <span class="post">Web前端开发工程师</span>
        <img class="portrait" src="https://q1.qlogo.cn/g?b=qq&nk=1937966358&s=100" alt="" />
      </div>
    </div>
    <div class="bottomBox">
      <div class="leftBox">
        <p>男 / 2000 四川成都</p>
        <p>专科 / 2022年毕业</p>
        <p>四川文化产业职业学院</p>
        <p>简介：一个对编程行业充满热情和憧憬的转行前端</p>
      </div>
      <div class="rightBox">
        <p>
          <a target="_blank" href="tel:15196923235">
            <span>15196923235</span> <i class="sg sg-phone"></i>
          </a>
        </p>
        <p>
          <a target="_blank" href="mailto:1937966358@qq.com">
            <span>1937966358@qq.com</span> <i class="sg sg-youxiang"></i>
          </a>
        </p>
        <p>
          <a target="_blank" href="https://timebk.cn/">
            <span>个人博客</span> <i class="sg sg-dingyue"></i>
          </a>
        </p>
        <p>
          <a target="_blank" href="https://blog.csdn.net/qq_19322833">
            <span>CSDN站</span> <i class="sg sg-csdn1"></i>
          </a>
        </p>
        <p>
          <a target="_blank" href="https://juejin.cn/user/770072696587341">
            <span>稀土掘金站</span> <i class="sg sg-signal"></i>
          </a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.topBox {
  border-bottom: 1px solid #fff;
  padding: 10px 0;
  display: flex;
  vertical-align: top;
  justify-content: space-between;
  align-items: center;

  >.leftBox {
    >.nameCn {
      font-size: 50px;
      letter-spacing: 2px;
    }

    >.nameEn {
      font-size: 25px;
      padding-left: 30px;
    }
  }

  >.rightBox {
    display: flex;
    vertical-align: top;
    align-items: center;

    >.post {
      font-weight: 300;
      font-size: 25px;
      padding-right: 20px;
    }

    >.portrait {
      border-radius: 50%;
      width: auto;
      height: 50px;
    }
  }
}

.myInforBox_mobile {

  >.topBox {
    display: block;
    text-align: center;

    >.leftBox {
      padding-bottom: 30px;
    }

    >.rightBox {
      justify-content: center;
    }

    >.bottomBox {
      display: block;
    }
  }

  >.bottomBox {
    display: block;

    >.rightBox {
      display: flex;
      vertical-align: top;
      justify-content: center;
      align-items: center;
      padding-top: 20px;

      >p {
        padding: 0 5px;

        >a {
          >span {
            display: none;
          }

          >i {
            font-size: 20px;
            padding: 5px;

          }
        }
      }
    }
  }
}

.bottomBox {
  line-height: 30px;
  padding: 15px 0 0 0;
  display: flex;
  vertical-align: top;
  justify-content: space-between;

  >.rightBox {
    text-align: right;
    font-size: 14px;

    >p {
      >a {
        >i {
          font-size: 12px;
          background: #fff;
          color: #00bdc4;
          border-radius: 50%;
          padding: 2px;
          font-weight: bold;
        }
      }
    }
  }
}
</style>