<template>
  <div class="TopBar">
    <i class="el-icon-location" />
    北京
    <router-link tag="span" :to="{name:'chengecity'}">切换城市</router-link>
    <div class="current-location">
      [
      <span>广东省</span>
      <span>惠州市</span>
      <span>惠城区</span>
      ]
    </div>
    <div class="m-user">
      <router-link tag="span" class="login" :to="{name:'login'}">立即登录</router-link>
      <router-link tag="span" :to="{name:'register'}">注册</router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less">
.TopBar {
  line-height: 40px;
  padding: 0 5px;
  display: inline-block;
  span{
    cursor: pointer;
    margin: 0 3px;
  color: #999;
  }
  span:hover{
    color: #FE8C00;
  }
  .current-location{
    display: inline;
  }
  .m-user {
    display: inline-block;
    margin-left: 20px;
  }
  .login{
    color: #FE8C00;
  }
}
</style>