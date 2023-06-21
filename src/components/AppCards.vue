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
        img{
            width: 100%;
            height: 170px;
            object-fit: cover;
            object-position: top;
        }
    }
</style>