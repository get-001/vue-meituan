<template>
  <ModalTabControl
    :title="data.title"
    :headColor="data.headColor"
    :tabs="data.tabs"
    style="margin-bottom:40px;"
  >
    <div class="ModalTabHaveStyle">
      <div class="quality-area" v-for="(item, index) in data.data" :key="index">
        <div class="quality-img">
          <img
            class="image"
            :src="item.imgUrl"
            onerror="this.src='https://p1.meituan.net/msmerchant/febed970aadd7af95503aa2e3b0d85b1466327.jpg@368w_208h_1e_1c'"
          />
        </div>
        <div class="poi-info">
          <div class="title" :title="item.title">{{item.title}}</div>
          <div class="sub-title" :title="item.subTitle">{{item.subTitle}}</div>
          <div class="price-info">
            <span class="current-price-wrapper">
              <span class="price-symbol numfont">¥</span>
              <span class="current-price numfont">{{item.currentPrice}}</span>
            </span>
            <span class="old-price">{{item.oldPrice}}</span>
            <span class="sold bottom-right-info">{{item.bottomInfo}}</span>
          </div>
        </div>
      </div>
      <!--  -->
    </div>
  </ModalTabControl>
</template>

<script>
import ModalTabControl from "./../ModalTabControl.vue";
export default {
  props: ["data"],
  components: { ModalTabControl }
};
</script>

<style lang="less">
.ModalTabHaveStyle {
  width: 100%;
  display: flex;
  flex-wrap: wrap;

  .quality-area {
    display: inline-block;
    width: 33%;
    flex-grow: 1;
    padding: 7px;
    font-size: 12px;
    transition: background-color 0.5s;
    cursor: pointer;

    .quality-img {
      height: 208px;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
    .poi-info {
      .title {
        margin: 11px 0 8px 0;
        font-size: 16px;
      }
      .sub-title {
        margin-bottom: 7px;
        color: #999;
      }
      .current-price-wrapper {
        .price-symbol {
          font-size: 14px;
          color: #f40;
        }
        .current-price {
          font-size: 22px;
          color: #f40;
          margin-right: 5px;
        }
      }
      .old-price {
        color: #999;
        text-decoration: line-through;
      }
      .bottom-right-info {
        color: #999;
        float: right;
        margin-top: 13px;
      }
    }
  }
  .quality-area:hover {
    background: #f4f4f4;
  }
}
</style>