<template>
  <div class="home">
    <HomePrimary />
    <HomeContent style="margin-top:40px;" />
  </div>
</template>

<script>
import HomePrimary from '@/components/Home/HomePrimary'
import HomeContent from '@/components/Home/HomeContent'

export default {
  name: "home",components:{HomePrimary,HomeContent}
};
</script>

<style lang="less">
</style>