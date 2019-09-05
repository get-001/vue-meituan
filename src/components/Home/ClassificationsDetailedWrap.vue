<template>
  <div class="ClassificationsDetailedWrap" :style="{top:y,left:x}">
    <div class="wrap" v-for="(item,index) in detail.leftPcHomeCategoryList" :key="index">
      <h2 class="head-title">
        <span class="title">{{item.name}}</span>
        <a :href="item.url" class="more float-right">
          更多
          <i class="nav-right-arrow"></i>
        </a>
      </h2>
      <ul class="body-list clearFloat" v-if="detail.rightPcHomeCategoryList">
        <li v-for="(item,index) in detail.rightPcHomeCategoryList[index]" :key="index">
          <a :href="item.url">{{item.name}}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ["detail", "y", "x"]
};
</script>

<style lang="less">
.ClassificationsDetailedWrap {
  z-index: 10;
  position: absolute;
  width: 400px;
  height: 416px;
  padding: 0 30px;
  background: #fff;
  cursor: default;
  left: 228px;
  top: 0;
  display: none;

  .wrap {
    .head-title {
      font-size: 16px;
      font-weight: 600;
      padding-top: 24px;
      padding-bottom: 10px;
      border-bottom: 1px solid #e5e5e5;
      line-height: 21px;
      a.more {
        font-size: 12px;
        color: #999;
      }
    }
    ul.body-list {
      li {
        float: left;
        margin-top: 10px;
        margin-right: 15px;
        a {
          color: #999;
        }
      }
      li:hover {
        color: #fe8c00;
        a {
          color: #fe8c00;
        }
      }
    }
  }
}
</style>