<template>
  <div id="app">
    <router-view />
  </div>
</template>
<script>
export default {
  created() {
    // this.$store.state.fullScreen = false;
    document.body.removeChild(document.getElementById("Loading"));
  }
};
</script>
<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
