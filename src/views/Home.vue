<template>
  <div class="home">
    <div class="boxLeft">
      <box-left />
    </div>
    <div class="boxRight">
      <box-right />
    </div>
  </div>
</template>
<script>
import boxLeft from "./boxLeft.vue";
import boxRight from "./boxRight.vue";
export default {
  components: {
    boxRight,
    boxLeft
  }
};
</script>
<style lang="less" scoped>
.home {
  width: 100%;
  height: 100vh;
  .boxLeft {
    width: 40%;
    height: 100%;
    float: left;
    position: relative;
  }
  .boxRight {
    width: 60%;
    height: 100%;
    float: left;
    position: relative;
  }
}
</style>