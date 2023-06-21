<script>
export default {
    props:{
        card: Object
    }
}
</script>
<template lang="">
    <div class="card">
        <img :src="card.thumb" alt="">
        <h4>{{ card.series }}</h4>
    </div>
</template>
<style lang="scss" scoped>
    .card{
        width: calc(100% / 6 - 20px);
        margin: 10px;
        display: flex;
        flex-direction: column;
        &:hover{
            cursor: pointer;
        }
        img{
            width: 100%;
            height: 170px;
            object-fit: cover;
            object-position: top;
        }
    }

    @media screen and (max-width: 992px) {
        .card{
            width: calc(100% / 4 - 20px);
        }
    }



    @media screen and (max-width: 768px) {
        .card{
            width: calc(100% / 3 - 20px);
        }
    }
</style>