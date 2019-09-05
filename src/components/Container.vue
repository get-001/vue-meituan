<template>
  <el-container class="wrapper">
    <el-header style="padding:0;height:197px;">
        <Header />
    </el-header>
    <el-main style="padding:0;margin:-50px;">
      <slot />
    </el-main>
    <el-footer>Footer</el-footer>
  </el-container>
</template>

<script>
import Header from "./Header/index.vue";
export default {
  components: {
    Header
  }
};
</script>