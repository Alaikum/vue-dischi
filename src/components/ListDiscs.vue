<template>
  <div>

    <LoadComp v-if="listDisc.length<10  || show===false " />
    <div class="main">
      <div class="container">
        <div class="row g-5">
          <div class="col_" v-for="(disc,i) in filterdSongs" :key="i">

            <DiscCard :info="disc" />
          </div>


        </div>

      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import DiscCard from "./DiscCard.vue";
import LoadComp from "./LoadComp.vue";

export default {
  data() {
    return {
      listDisc: [],
      show: false,
      contatore: 0
    };
  },
  props: {
    musicGenre: {
      type: String,
      default: ''
    }
  },
  computed:{
    filterdSongs(){
      return this.listDisc.filter((el)=>{
        const genre=el.genre.toLowerCase()
        const find= this.musicGenre.toLowerCase()
        if(genre.includes(find)){
          return true
        }
        return false
      })
    }

  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        console.log(res.data.response);
        this.listDisc = res.data.response;
        // console.log(this.listDisc);
      })
      .catch((err) => {
        console.log("Error", err);
      })
      .finally(() => {
        console.log("Finito");
        this.visibile()
      });
  },
  methods: {
    visibile() {
      setTimeout(() => {
        this.contatore++
        console.log('lanciata', +this.contatore)
        this.show = true
        console.log(this.show)
      }, 2000)

    }

  },
  components: { DiscCard, LoadComp }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/general.scss";

.main {
  background-color: $--main-color;
  transform: translateY(80px);



  .container {
    background-color: $--second-color;

    .row {
      background-color: $--main-color;
      justify-content: center;

      .col_ {
        flex-basis: calc(100% /5);
        // background-color: $--main-color;
        transition: all ease-in 0.5s;

        &:hover {

          cursor: pointer;
        }
      }
    }
  }
}
</style>
