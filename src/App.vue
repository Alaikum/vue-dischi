<template>
  <div id="app">
    <HeaderAndLogo />
    <ListDiscs />

  </div>
</template>

<script>
import ListDiscs from './components/ListDiscs.vue'
import HeaderAndLogo from './components/headerAndLogo.vue';

export default {
  name: 'App',
  components: {
    ListDiscs,
    HeaderAndLogo
  }
}
</script>

<style lang="scss">
@import "../src/style/general.scss";
#app{
  background-color: $--main-color;
}
</style>
