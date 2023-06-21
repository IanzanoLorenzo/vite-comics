<script>
import AppJumbotron from './AppJumbotron.vue';
import cards from '../data/dc-comics.json';
export default {
    components:{
        AppJumbotron
    }

}
</script>
<template lang="">
    <AppJumbotron/>
    <div class="content">
        <div class="container">
            
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .content{
        height: 100px;
        background-color: black;
        color: white;
        .container{
            height: 100%;
            display: flex;
            align-items: center;
        }
    }
</style>
