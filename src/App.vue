<template>
  <div id="app">

    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="text-center">ciao</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
@import "../src/style/general.scss";

</style>
