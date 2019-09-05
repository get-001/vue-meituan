<template>
  <div class="ModalTabControl">
    <div class="Control-head">
      <h2 class="headline">猜你喜欢</h2>
      <ul class="tab-view clearFloat">
        <li>全部</li>
        <li>约会聚餐</li>
        <li>丽人SPA</li>
        <li>品质出游</li>
      </ul>
    </div>
    <div class="Control-body"></div>
  </div>
</template>



<style lang="less" scoped>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
}

.ModalTabControl {
  margin-bottom: 40px;
  .Control-head {
    color: #fff;
    height: 44px;
    border-radius: 6px 6px 0 0;

    background: linear-gradient(
        to right,
        rgb(18, 210, 198) 2%,
        rgb(14, 190, 212) 97%
      )
      rgb(18, 210, 198);

    .headline {
      display: inline-block;
      font-size: 16px;
      margin-left: 13px;
      margin-right: 10px;
      line-height: 44px;
    }
    ul.tab-view {
      display: inline-block;
      font-size: 15px;
      vertical-align: top;
      li {
        float: left;
        line-height: 44px;
        padding: 0 5px;
        cursor: pointer;
      }
    }
  }
  .Control-body {
    height: 500px;
    background: #fff;
    border-radius: 0 0 6px 6px;
    border-left: 1px solid #e5e5e5;
    border-right: 1px solid #e5e5e5;
    border-bottom: 1px solid #e5e5e5;
    padding: 10px;
  }
}
</style>