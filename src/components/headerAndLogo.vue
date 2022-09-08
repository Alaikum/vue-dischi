<template>
    <div class="header">
        <img src="../assets/logoSpot.png" alt="">

        <select class="rounded" v-model="genere" name="" id="" @change="$emit('search', genere)">
            <option value="">Tutti i Generi</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>

export default {
    data() {
        return {
            genere: ''
        }
    }

}
</script>

<style scoped lang="scss">
@import "../style/general.scss";

.header {
    color: cyan;
    height: 70px;
    background-color: $--second-color;
    display: flex;
    justify-content: space-between;

    img {
        max-height: 100%;
        padding: 10px 20px;
        transition: all ease-in 0.5s;

        &:hover {
            scale: 1.5;
            cursor: pointer;
        }

    }

    select {
        max-height: 40px;
        align-self: center;
        font-size: 2rem;
        background-color: $--second-color;
        color: white;
        text-transform: uppercase;

        &:hover {
            cursor: pointer;
           color: cyan;
        }

    }

}
</style>