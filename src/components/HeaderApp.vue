<script>
export default {
    data() {
        return {
            links: [
                {
                    title: 'CHARACTERS',
                    href: '/',
                    active: false
                },
                {
                    title: 'COMICS',
                    href: '/',
                    active: true
                },
                {
                    title: 'MOVIES',
                    href: '/',
                    active: false
                },
                {
                    title: 'TV',
                    href: '/',
                    active: false
                },
                {
                    title: 'GAMES',
                    href: '/',
                    active: false
                },
                {
                    title: 'COLLECTIBLES',
                    href: '/',
                    active: false
                },
                {
                    title: 'VIDEOS',
                    href: '/',
                    active: false
                },
                {
                    title: 'FANS',
                    href: '/',
                    active: false
                },
                {
                    title: 'NEWS',
                    href: '/',
                    active: false
                },
                {
                    title: 'SHOP',
                    href: '/',
                    active: false
                },
            ]
        }
    },
}
</script>
<template lang="">
    <div>
        <nav>
            <div class="container">
                <div class="row">
                    <img src="/img/dc-logo.png" alt="" />
                    <ul>
                        <li v-for="(link, index) in links" :key="index" :class="link.active ? 'active' : ''"><a :href="link.href">{{link.title}}</a></li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/varables' as *;
nav{
    width: 100%;
    display: flex;
    .row{
        display: flex;
        align-items: center;
        justify-content: space-between;
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
                &.active{
                    color: $color_primary;
                    border-bottom: $color_primary 7px solid;
                    border-top: transparent 7px solid;
                }
            }
        }
    }
    
}
</style>