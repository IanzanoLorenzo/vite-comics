<script>
import AppJumbotron from './AppJumbotron.vue';
import AppCards from './AppCards.vue';
import cards from '../data/dc-comics.json';
export default {
    components:{
        AppJumbotron,
        AppCards
    },
    data() {
        return {
            cards
        }
    },

}
</script>
<template lang="">
    <main>
        <AppJumbotron/>
    <div class="container">
        <AppCards v-for="(card, index) in cards" :key="index" :card="card" />
        <div class="row">
            <button><h3>LOAD MORE</h3></button>
        </div>
    </div>
    </main>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
main{
    background-color: $color-bg-secondary;
    color: white; 
}    
.container{
    display: flex;
    flex-wrap: wrap;
    margin-top: 30px;
    .row{
        display: flex;
        width: 100%;
        justify-content: center;
        button{
            color: white;
            background-color: $color-primary;
            border: $color-primary;
            padding: 10px 50px;
            margin: 30px;
        }
    }
}
</style>
