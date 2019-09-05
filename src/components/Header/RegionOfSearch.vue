<template>
  <div class="RegionOfSearch">
    <div class="logo">
      <CenterWrap>
        <div class="box-logo">
          <img src="https://s0.meituan.net/bs/fe-web-meituan/fa5f0f0/img/logo.png" alt="美团网" />
        </div>
        <div class="box-search">
          <div class="row search">
            <input type="text" placeholder="搜索商家或地点" />
            <button>
              <i class="el-icon-search"></i>
            </button>
          </div>
          <ul class="header-search-hotword">
            <li>红花胡水上乐园</li>
            <li>欧美城文化小镇</li>
            <li>双月湾</li>
            <li>云顶温泉度假村</li>
            <li>巽寮湾</li>
            <li>惠州演达酒店</li>
            <li>有名肠</li>
          </ul>
        </div>
      </CenterWrap>
    </div>
  </div>
</template>

<script>
import CenterWrap from "@/components/reusable/CenterWrap";
export default {
  components: { CenterWrap }
};
</script>

<style lang="less">
.RegionOfSearch {
  height: 122px;
  // padding-bottom: 35px;
  .box-logo {
    width: 280px;
    height: 100%;
    padding: 37px 0;
    padding-right: 40px;
    img {
      width: 126px;
      height: 45px;
      object-fit: cover;
    }
  }
  .box-search {
    height: 100%;
    //
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    .search {
      width: 550px;
      margin-top: 28px;
      // background: rgba(255, 0, 0, 0.2);
      height: 40px;
      input {
        vertical-align: top;
        width: 85.44%;
        height: 40px;
        outline: none;
        border-radius: 4px 0 0 4px;
        border: 1px solid #e5e5e5;
        padding: 10px 10px;
      }
      button {
        vertical-align: top;
        width: 14.55%;
        line-height: 40px;
        border-radius: 0 4px 4px 0;
        background: #ffc300;
        border: none;
        cursor: pointer;
        outline: none; //消除默认点击蓝色边框效果
        i {
          font-size: 26px;
          vertical-align: middle;
        }
      }
    }
    ul.header-search-hotword {
      padding-top: 8px;
      padding-left: 12px;
      color: #666;
      li {
        display: inline-block;
        margin: 0 4px;
        cursor: pointer;
      }
      li:hover {
        color: #ffc300;
      }
    }
  }
}
</style>