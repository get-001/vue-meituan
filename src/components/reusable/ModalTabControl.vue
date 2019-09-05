<template>
  <div class="ModalTabControl">
    <div class="Control-head" :style="{'background':headColor}">
      <h2 class="headline">{{title}}</h2>
      <ul class="tab clearFloat">
        <li :class="{active:active===index}" v-for="(item, index) in tabs" :key="index" @mouseenter="selectionPages(index)">{{item.text}}</li>
      </ul>
    </div>
    <div class="Control-body">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
    props:['title','tabs','headColor'],
    data() {
        return {
            active:0
        }
    },
    methods:{
        selectionPages(index){
            this.active=index;
            this.$emit('selectionPages',index)
        }
    }
}
</script>

<style lang="less" scoped>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
}

.ModalTabControl {
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
    ul.tab {
      display: inline-block;
      font-size: 15px;
      vertical-align: top;
      li {
        float: left;
        line-height: 44px;
        padding: 0 5px;
        cursor: pointer;
        position: relative;
        overflow: hidden;
      }
      li.active::after{
          position: absolute;
          bottom: -17px;
          left: 50%;
          content: "";
          display: inline-block;
          width: 20px;
          height: 20px;
          background: #fff;
          transform: translateX(-50%) rotate(45deg);
      }
    }
  }
  .Control-body {
    background: #fff;
    border-radius: 0 0 6px 6px;
    border-left: 1px solid #e5e5e5;
    border-right: 1px solid #e5e5e5;
    border-bottom: 1px solid #e5e5e5;
    padding: 10px;
  }
}
</style>