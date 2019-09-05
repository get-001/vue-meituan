<template>
  <div class="NavigationBar">
    <CenterWrap class="clearFloat">
      <TopBar class="float-left" />
      <SearchBar class="float-right" />
    </CenterWrap>
  </div>
</template>

<script>
import CenterWrap from "@/components/reusable/CenterWrap";
import TopBar from "./TopBar";
import SearchBar from "./SearchBar";

export default {
  components: { CenterWrap, TopBar, SearchBar }
};
</script>

<style lang="less">
.NavigationBar {
  height: 40px;
  background: #f8f8f8;
  color: #999;
  a {
    color: #999;
  }
  a:hover {
    color: #fe8c00;
  }
}
</style>