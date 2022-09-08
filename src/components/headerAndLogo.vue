<template>
    <div class="header">
       <img src="../assets/logoSpot.png" alt="">
    
    </div>
</template>

<script>

export default {

}
</script>

<style scoped lang="scss">
    @import "../style/general.scss";
.header {
    color: cyan;
    height: 70px;
    background-color: $--second-color;
   
    img{
        max-height: 100%;
        padding: 10px 20px;
        transition: all ease-in 0.5s;
        &:hover{
            scale: 1.5;
            cursor: pointer;
        }
        
    }
   
}
</style>