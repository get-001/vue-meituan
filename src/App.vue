<template>
  <div id="app">
    <!-- <nav>
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </nav>-->
    <Container>
      <CenterWrap>
        <router-view />
      </CenterWrap>
    </Container>
  </div>
</template>

<script>
import Container from "@/components/Container";
import CenterWrap from "@/components/reusable/CenterWrap";

export default {
  components: { Container, CenterWrap }
};
</script>

<style lang="less">
.clearFloat::after {
  content: "";
  clear: both;
  display: block;
}
</style>