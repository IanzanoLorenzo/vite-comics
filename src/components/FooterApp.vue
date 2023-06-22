<script>
import AppBlueSection from './AppBlueSection.vue';
export default {
    components: {
        AppBlueSection
    },
    data() {
        return {
            listsBottomMenu: [
                {
                    listName: 'DC COMICS',
                    listContent:[
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    listName: 'SHOP',
                    listContent:[
                        'Shop DC',
                        'Shop DC Collectibles',
                    ]
                },
                {
                    listName: 'DC',
                    listContent:[
                        'Terms Of Use',
                        'Privacy Policy',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Talent Workshop',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    listName: 'DC COMICS',
                    listContent:[
                        'DC',
                        'MAD Magazine',
                        'DC Kidz',
                        'DC Universe',
                        'DC Power Visa'
                    ]

                }
            ],
            socials : [
                'facebook',
                'periscope',
                'pinterest',
                'twitter',
                'youtube'
            ]
        }
    },
}
</script>
<template lang="">
    <footer>
        <AppBlueSection />
        <div class="bottom-menu">
            <div class="container">
                <ul v-for="(list, index) in listsBottomMenu" :key="index" class="list-Title"><h3>{{ list.listName }}</h3>
                    <li v-for="(listItem, index) in list.listContent" :key="index"><a href="">{{ listItem }}</a></li>
                </ul>
            </div>    
        </div>
        <div class="info-footer">
            <div class="container">
                <button>SIGN-UP NOW</button>
                <div class="socials">
                    <h2>FOLLOW US</h2>
                    <img v-for="(social, index) in socials" :key="index" :src="`/footer-${socials[index]}.png`" alt="pippo">
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .bottom-menu{
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;
        color: white;
        h3{
            margin-bottom: 1rem;
        }
        ul{
            margin: 1rem 0 0 0;
            width: 200px;
        }
        li{
            color: gray;
            font-size: 14px;
            margin: 0.5rem;
            margin-left: 0;
        }
        .container{
            background-image: url('../assets/img/dc-logo-bg.png');
            background-size: 32rem;
            background-repeat: no-repeat;
            background-position: right;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            max-height: 430px;
            justify-items: center;
            align-content: flex-start;
            padding: 2rem 0;
        }


    }
    .info-footer{
        color: white;
        background-color: $color-gray;
        .container{
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        button{
            background-color: transparent;
            color: inherit;
            padding: 10px 20px;
            border: $color-primary 2px solid;
            margin: 20px 0;
        }
        .socials{
            display: flex;
            align-items: center;
            flex-direction: row;
            img{
                margin: 10px;
                transition: all .2s linear;
                &:hover{
                    filter: brightness(2);
                }
            }
            h2{
                color: $color-primary;
            }
        }
    }
    @media screen and (max-width: 992px) {

    }     
    @media screen and (max-width: 768px) {
        .container{
            flex-direction: column;
        }
        .bottom-menu{
            .container{
                max-height: none ;
                align-content: center;
            }
        }
    }
</style>