<template>

    <div class="card p-3">
      <img class="card-img-top" :src="info.poster" alt="info.title">
        <div class="card-body text-center">
            <h4 class="card-title ">{{info.title}}</h4>
            <p class="card-text">{{info.author}} <br/> {{info.year}}</p>
        </div> 
        
       
     
    </div>
</template>


<script>
export default {
    props:{
        info: Object
    },

}
</script>

<style scoped lang="scss">
    i{color: white}
    @import "../style/general.scss";
.card{
    border: none;
    max-width: 200px;
    min-width: 185px;
    height: 360px;
    background-color: $--second-color;
   
img{
    transition: all ease-in 0.5s;
        &:hover{
            scale: 1.5;
            border-radius: 50%;
            cursor: pointer;
        }
}
    h4{
        color: white;
        text-transform: uppercase;
    }

    p{
        color: grey;
        font-size: 1.125rem;
    }
}
</style>