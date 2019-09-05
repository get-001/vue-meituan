<template>
  <div class="HomeContent">
    <ModalTabHaveStyle :data="qualityData" />
    <ModalTabHaveStyle :data="qualityData" />
  </div>
</template>

<script>
import { quality } from "./data.js";
import ModalTabHaveStyle from "@/components/reusable/ModalTab/ModalTabHaveStyle";

export default {
  components: { ModalTabHaveStyle },
  mounted() {
    console.log(quality);
    // https://p1.meituan.net/msmerchant/febed970aadd7af95503aa2e3b0d85b1466327.jpg@368w_208h_1e_1c
    // https://img.meituan.net/w.h/msmerchant/9413e6531f1a279426692ee66b51cb3c82331.jpg
  },
  computed: {
    qualityData() {
      quality.title = "有格调";
      quality.headColor = "rgb(194, 176, 142)";
      const reg = /https:\/\/img\.meituan\.net\/w\.h(\/msmerchant\/[\w]+\.jpg)/g;
      quality.data.forEach(ele => {
        ele.imgUrl=ele.imgUrl.replace(
          reg,
          ($, $1) => "https://p1.meituan.net" + $1 + "@368w_208h_1e_1c"
        );
      });
      return quality;
    }
  }
};
</script>