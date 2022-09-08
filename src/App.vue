<template>
  <div id="app">

    <HeaderAndLogo @search="musicalGenre" />
 
    <ListDiscs :musicGenre="genreProp" />

  </div>
</template>

<script>
import ListDiscs from './components/ListDiscs.vue'
import HeaderAndLogo from './components/headerAndLogo.vue';


export default {
  name: 'App',
  components: {
    ListDiscs,
    HeaderAndLogo,

  },
  data() {
    return {
      genreProp: ''
    }
  },
  methods: {
    musicalGenre(data) {
      console.log(data)
      this.genreProp = data
    }
  }


}
</script>

<style lang="scss">
@import "../src/style/general.scss";

#app {
  background-color: $--main-color;
}


</style>
