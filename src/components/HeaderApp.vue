<script>
export default {
    data() {
        return {
            menuShow: false,
            activePage: 0,
            vociMenu: [
                {
                    title: 'CHARACTERS',
                    href: '',
                },
                {
                    title: 'COMICS',
                    href: '',
                },
                {
                    title: 'MOVIES',
                    href: '',
                },
                {
                    title: 'TV',
                    href: '',
                },
                {
                    title: 'GAMES',
                    href: '',
                },
                {
                    title: 'COLLECTIBLES',
                    href: '',
                },
                {
                    title: 'VIDEOS',
                    href: '',
                },
                {
                    title: 'FANS',
                    href: '',
                },
                {
                    title: 'NEWS',
                    href: '',
                },
                {
                    title: 'SHOP',
                    href: '',
                },
            ]
        }
    },
    methods: {
        setActivePage(index){
            this.activePage = index
        },
        activeMenu(){
            this.menuShow = !this.menuShow
        }
    },
}
</script>
<template lang="">
    <header>
        <nav>
            <div class="container">
                <div class="row">
                    <div class="logo">
                        <img src="/dc-logo.png" alt="" />
                        <button @click="activeMenu()"><h3>Menu</h3></button>
                    </div>
                    <ul :class="menuShow ? '' : 'hide'">
                        <li @click="setActivePage(index)" v-for="(element, index) in vociMenu" :key="index" :class="activePage === index ? 'active' : ''">{{element.title}}</li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
nav{
    width: 100%;
    display: flex;
    .row{
        display: flex;
        align-items: center;
        justify-content: space-between;
        .logo{
            display: flex;
            align-items: center;
        }
        button{
            display: none;
            background-color: $color-primary ;
            border: $color-primary;
            padding: 10px 30px;
            color: white;

        }
        img{
            height: 70px;
        }
        ul{
            list-style: none;
            display: flex;
            li{
                list-style: none;
                padding: 0 10px;
                font-size: 12px;
                display: flex;
                align-items: center;
                justify-content: center;
                height: 80px;
                a{
                    color: inherit;
                    text-decoration: none;
    
                }
                &:hover{
                    color: $color_primary;
                    cursor: pointer;
                }
                &.active{
                    color: $color_primary;
                    border-bottom: $color_primary 7px solid;
                    border-top: transparent 7px solid;
                }
            }
        }
    }
    
}


@media screen and (max-width: 992px) {
}     
@media screen and (max-width: 768px) {
    nav {
        position: fixed;
        z-index: 2;
        top: 0;
        left: 0;
        right: 0;
        background-color: rgba(255, 255, 255, 0.747);
        .row{
            justify-content: center; 
            align-items: center;
            flex-direction: column;
            .logo{
                width: 100%;
                background-color: white;
            }
            ul{
                flex-wrap: wrap;
                overflow: hidden;
                transition: all  linear;
                &.hide{
                    height: 0;
                }
            }
            button{
                display: inline-block;
            }
            img{
                margin: 5px 50px;
            }
        }
    }
}
</style>