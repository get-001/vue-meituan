<template>
  <div class="Primary">
    <div class="all-classifications">
      <div class="btn-title">全部分类</div>
      <ul class="list-content" v-if="categorys">
        <li
          class="list"
          @mouseover="openSortlist(index)"
          v-for="(item,index) in categorys"
          :key="index"
        >
          <i class="icon" :class="iconArr[index]"></i>
          <span class="link" v-for="item in item.leftPcHomeCategoryList" :key="item.id">
            <a :href="item.url" target="_blank">{{item.name}}</a>
          </span>
          <i class="nav-right-arrow"></i>
        </li>
        <ClassificationsDetailedWrap :detail="detail" y="60px" />
      </ul>
    </div>
    <div class="right-banner">
      <ul class="nav-links">
        <li>
          <a href="#">美团外卖</a>
        </li>
        <li>
          <a href="#">猫眼电影</a>
        </li>
        <li>
          <a href="#">美团酒店</a>
        </li>
        <li>
          <a href="#">猫眼电影</a>
        </li>
        <li>
          <a href="#">民宿/公寓</a>
        </li>
        <li>
          <a href="#">商家入驻</a>
        </li>
        <li>
          <a href="#">美团公益</a>
        </li>
      </ul>
      <div class="advertising-image-wrap">
        <div class="row-wrap-top">
          <div class="box slideshow">
            <div class="block">
              <el-carousel height="240px" :interval="3000">
                <el-carousel-item v-for="(item,index) in slideshowData" :key="index">
                  <img :src="item.imgUrl" />
                </el-carousel-item>
              </el-carousel>
            </div>
          </div>
          <div class="box img-ad-min"></div>
          <div class="box personal-center">
            <div class="head-portrait">
              <img src="//s0.meituan.net/bs/fe-web-meituan/e350c4a/img/avatar.jpg" />
            </div>
            <p class="user-name">Hi！你好</p>
            <div class="row-btn">
              <div class="btn btn-register">注册</div>
            </div>
            <div class="row-btn">
              <div class="btn btn-login">立即登陆</div>
            </div>
          </div>
        </div>
        <div class="row-wrap-bottom">
          <div class="box img-ad-max"></div>
          <div class="box img-ad-max"></div>
          <div class="box img-ad-min"></div>
          <div class="box meituan-app">
            <div class="qrcode-box">
              <img src="//s1.meituan.net/bs/fe-web-meituan/60ac9a0/img/download-qr.png" alt="下载APP" />
            </div>
            <p class="app-name">美团APP手机版</p>
            <p class="sl">
              <span class="red">1元起</span>
              <span class="gary">吃喝玩乐</span>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ClassificationsDetailedWrap from "./ClassificationsDetailedWrap";
import { AppData } from "./data.js";

export default {
  components: { ClassificationsDetailedWrap },
  mounted() {
    // console.log(AppData);
    console.log(this.categorys);
  },
  data() {
    return {
      slideshowData: [
        {
          imgUrl:
            "http://p0.meituan.net/codeman/daa73310c9e57454dc97f0146640fd9f69772.jpg"
        },
        {
          imgUrl:
            "http://p1.meituan.net/codeman/826a5ed09dab49af658c34624d75491861404.jpg"
        },
        {
          imgUrl:
            "http://p0.meituan.net/codeman/a97baf515235f4c5a2b1323a741e577185048.jpg"
        },
        {
          imgUrl:
            "http://p0.meituan.net/codeman/33ff80dc00f832d697f3e20fc030799560495.jpg"
        },
        {
          imgUrl:
            "https://p1.meituan.net/travelcube/01d2ab1efac6e2b7adcfcdf57b8cb5481085686.png"
        }
      ],
      detail: { leftPcHomeCategoryList: [], rightPcHomeCategoryList: [] },
      iconArr: [
        "hc-icon-foodNew",
        "hc-icon-waimaiNew",
        "hc-icon-hotelNew",
        "hc-icon-zhenguoNew",
        "hc-icon-maoyanNew",
        "hc-icon-planeNew",
        "hc-icon-ktvNew",
        "hc-icon-lifeNew",
        "hc-icon-beautyNew",
        "hc-icon-marriedNew",
        "hc-icon-childNew",
        "hc-icon-sportNew",
        "hc-icon-decorateNew",
        "hc-icon-educationNew",
        "hc-icon-medicalNew",
        "hc-icon-barNew"
      ]
    };
  },
  computed: {
    categorys() {
      return AppData.categorys;
    }
  },
  methods: {
    openSortlist(index) {
      this.detail = this.categorys[index];
    }
  }
};
</script>

<style lang="less">
.Primary {
  position: relative;
  display: flex;

  .all-classifications {
    background: #fff;
    width: 228px;
    border: 1px solid #e5e5e5;
    cursor: default;

    .btn-title {
      padding-left: 15px;
      font-size: 16px;
      font-weight: 600;
      line-height: 50px;
    }
    ul.list-content {
      margin: 10px 0;
      color: #666;

      li.list {
        line-height: 22px;
        padding: 2px 12px;
        a {
          color: #666;
        }
        span.link::after {
          content: "/";
          margin: 0 3px;
        }
        span.link:last-of-type::after {
          content: "";
          margin: 0;
        }
      }
      li.list {
        .icon {
          margin-right: 10px;
        }
        .hc-icon-foodNew:before {
          content: "\e60e";
          color: #ff8200;
        }
        .hc-icon-waimaiNew:before {
          content: "\e60a";
          color: #ffb500;
        }
        .hc-icon-hotelNew:before {
          content: "\e616";
          color: #9b5e3e;
        }
        .hc-icon-zhenguoNew:before {
          content: "\e60c";
          color: #ffb500;
        }
        .hc-icon-maoyanNew:before {
          content: "\e612";
          color: #ff3d00;
        }
        .hc-icon-planeNew:before {
          content: "\e615";
          color: #03a9f4;
        }
        .hc-icon-ktvNew:before {
          content: "\e607";
          color: #00bf96;
        }
        .hc-icon-lifeNew:before {
          content: "\e614";
          color: #00bf96;
        }
        .hc-icon-beautyNew:before {
          content: "\e60f";
          color: #ff4081;
        }
        .hc-icon-marriedNew:before {
          content: "\e609";
          color: #ff4081;
        }
        .hc-icon-childNew:before {
          content: "\e608";
          color: #ff4081;
        }
        .hc-icon-sportNew:before {
          content: "\e611";
          color: #03a9f4;
        }
        .hc-icon-decorateNew:before {
          content: "\e60b";
          color: #00bf96;
        }
        .hc-icon-educationNew:before {
          content: "\e610";
          color: #00bf96;
        }
        .hc-icon-medicalNew:before {
          content: "\e60d";
          color: #03a9f4;
        }
        .hc-icon-barNew:before {
          content: "\e606";
          color: #00bf96;
        }
      }
      li.list:hover {
        background: rgba(255, 150, 0, 0.08);
        color: #222222;
        a {
          color: #222222;
          font-weight: 600;
        }
        i.nav-right-arrow::before,
        i.nav-right-arrow::after {
          background: #222222;
        }
      }
    }
    ul.list-content:hover > .ClassificationsDetailedWrap {
      display: block;
    }
  }
  .right-banner {
    width: calc(100% - 228px);
    position: relative;
    ul.nav-links {
      position: absolute;
      top: 15px;
      left: 20px;
      li {
        display: inline-block;
        margin: 0 20px;
        font-size: 16px;
        font-weight: 600;
        cursor: pointer;
        a {
          color: #222222;
          font-weight: 600;
        }
      }
      li:hover {
        a {
          color: #fe8c00;
        }
      }
    }
    .advertising-image-wrap {
      margin-top: 50px;
      height: 438px;
      padding-top: 10px;
      padding-left: 10px;
      .row-wrap-top {
        height: 240px;
        .img-ad-min {
          background-image: url("http://p0.meituan.net/codeman/e473bb428f070321269b23370ff02ba956209.jpg");
        }
      }
      .row-wrap-bottom {
        margin-top: 10px;
        height: 165px;
        .img-ad-max:nth-of-type(1) {
          background-image: url("http://p1.meituan.net/codeman/8cce56c467a17e04f3094d1e455462a0132772.png");
        }
        .img-ad-max:nth-of-type(2) {
          background-image: url("http://p1.meituan.net/codeman/16442c19da1f1c4544f794e29d99c92051716.jpg");
        }
        .img-ad-min {
          background-image: url("http://p1.meituan.net/codeman/5b21cddb4bb1cbc3a9c3bce0f726c75940469.jpg");
        }
      }
      .box {
        display: inline-block;
        height: 100%;
        background: #fff;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
      }

      .slideshow {
        width: 550px;
        margin-right: 10px;
        overflow: hidden;
        img {
          width: 100%;
          height: 100%;
        }
      }
      .img-ad-min {
        width: 150px;
        margin-right: 10px;
      }
      .img-ad-max {
        width: 270px;
        margin-right: 10px;
      }
      .img-ad-min {
        width: 150px;
        margin-right: 10px;
      }
      .personal-center {
        width: 230px;
        overflow: hidden;
        padding-top: 30px;
        .head-portrait {
          height: 60px;
          margin-bottom: 5px;
          img {
            margin: 0 auto;
            display: block;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
          }
        }
        p.user-name {
          text-align: center;
          font-size: 16px;
        }
        .row-btn {
          .btn {
            margin: 0 auto;
            width: 118px;
            line-height: 38px;
            border: 1px solid #e5e5e5;
            text-align: center;
            border-radius: 30px;
            margin-top: 10px;
            cursor: pointer;
            transition: background-color 0.5s;
          }
          .btn:hover {
            background-color: #f6f6f6;
          }
        }
      }
      .meituan-app {
        width: 230px;
        overflow: hidden;
        .qrcode-box {
          padding-top: 10px;
          img {
            width: 95px;
            height: 95px;
            margin: 0 auto;
            display: block;
          }
        }
        p {
          text-align: center;
          .red {
            color: red;
            margin-right: 5px;
          }
        }
        p.app-name {
          font-weight: 600;
          font-size: 16px;
          margin: 5px 0;
        }
      }
    }
  }
}
</style>