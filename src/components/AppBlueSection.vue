<script>
export default {
    data() {
        return {
            sections: [
                {
                    sectionName:'DIGITAL COMICS',
                    sectionImage: 'buy-comics-digital-comics.png'
                },
                {
                    sectionName:'DC MERCHANDAISE',
                    sectionImage: 'buy-comics-merchandise.png'
                },
                {
                    sectionName:'SUBSCRIPTON',
                    sectionImage: 'buy-comics-shop-locator.png'
                },
                {
                    sectionName:'COMICS SHOP LOCATION',
                    sectionImage: 'buy-comics-subscriptions.png'
                },
                {
                    sectionName:'DC POWER VISA ',
                    sectionImage: 'buy-dc-power-visa.svg'
                },
            ]
        }
    },
    
}
</script>
<template lang="">
    <div class="blue-section">
        <div class="container">
            <ul class="sections-list">
                <li v-for="(section, index) in sections" :key="index">
                    <img class="" :src="`../src/assets/img/${section.sectionImage}`" alt="immagine">
                    <div class=""><a href="">{{ section.sectionName }}</a></div>
                </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    .blue-section{
        background-color: $color-primary;
    }
    .sections-list{
        color: white;
        display: flex;
        width: 100%;
        align-items: center;
        justify-content: space-between;
        li{
            display: flex;
            align-items: center;
            margin: 20px 10px;
            img{
                height: 50px;
                margin: 5px 10px;
            }

        }
    }
</style>