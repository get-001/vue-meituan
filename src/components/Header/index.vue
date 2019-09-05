<template>
  <div class="Header">
    <NavigationBar />
    <region-of-search />
  </div>
</template>

<script>
import NavigationBar from "./NavigationBar";
import RegionOfSearch from "./RegionOfSearch";

export default {
  components: {
    NavigationBar,RegionOfSearch
  }
};
</script>

<style lang="less">
  .Header{
    height:197px;
    background: #fff;
    box-shadow: 0 2px 27px 0 rgba(0,0,0,0.10);
  }
</style>