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
                    sectionImage: 'buy-comics-subscriptions.png'
                },
                {
                    sectionName:'COMICS SHOP LOCATION',
                    sectionImage: 'buy-comics-shop-locator.png'
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
            <ul>
                <li v-for="(section, index) in sections" :key="index">
                    <img class="" :src="`/${section.sectionImage}`" alt="immagine">
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
    ul{
        color: white;
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        align-items: center;
        justify-content: space-evenly;
        li{
            display: flex;
            align-items: center;
            margin: 20px 10px;
            img{
                height: 50px;
            }
            &:last-child img{
            margin: 5px 10px;
            height: 35px;
            }
            
        }
    }
    @media screen and (max-width: 992px) {
        ul{
            width: fit-content;
            li{
                width: calc(100% / 3 - 20px);
            }
        }
        
    }
    
    @media screen and (max-width: 768px) {
        .container{
            display: flex;
            justify-content: center;
        }
        ul{
            flex-direction: column;
            align-items: center;
            li{
                width: calc(100% - 20px);
            }
        }
    }
</style>