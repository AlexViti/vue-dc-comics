<template>
  <div id="app">
    <HeaderDc />
    <MainDc />
  </div>
</template>

<script>
import HeaderDc from "./components/HeaderDc.vue";
import MainDc from "./components/MainDc.vue";

export default {
  name: "App",
  components: {
    HeaderDc,
    MainDc,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/style";

#app {
  min-height: 100vh;
  background-color: $darker_gray;
}
</style>
