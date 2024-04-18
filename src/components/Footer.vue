<template>
    <div class="footer">
        <div class="footer-main">
            <div class="footer-main__logo">
                <img src="svg/logo.svg" alt="castaway">
            </div>
            <ul class="footer-main__list">
                <li class="footer-main__item" v-for="(component, i) of social" :key="i">
                    <a :href="component.link">
                        <img :src="component.img" :alt="component.name">
                    </a>
                </li>
            </ul>
        </div>
            <ul class="footer-menu__list">
                <li class="footer-menu__item" v-for="(component, i) of nav" :key="i">
                    <a :href="component.link">
                        {{ component.name }}
                    </a>
                </li>
            </ul>
            <ul class="footer-menu__list">
                <li class="footer-menu__item" v-for="(component, i) of docs" :key="i">
                    <a :href="component.link"> 
                        {{ component.name }}
                    </a>
                </li>
            </ul>
        <div class="footer-media">
            <Media />
        </div>
    </div>
</template>

<script setup>
import Media from './Blocks/Media.vue';
const nav = [
    {
        name: 'Home',
        link: '/Home'
    },
    {
        name: 'Episodes',
        link: '/Episodes'
    },
    {
        name: 'About',
        link: '/About'
    },
    {
        name: 'Contact',
        link: '/Contact'
    },
]
const social = [
    {
        name:'Instagram',
        img: 'svg/instagram.svg',
        link: '/'
    },
    {
        name:'Twitter',
        img: 'svg/twitter.svg',
        link: '/'
    },
    {
        name:'Facebook',
        img: 'svg/facebook.svg',
        link: '/'
    },
]
const docs =[
    {
        name: 'Style Guide',
        link: '/Style Guide'
    },//1
    {
        name: 'Instructions',
        link: '/Instructions'
    },//2
    {
        name: 'Changelog',
        link: '/Changelog'
    },//3
    {
        name: 'Credit',
        link: '/Credit'
    },//4
    {
        name: 'Powered by Webflow',
        link: '/Powered by Webflow'
    },//5
    {
        name: 'Licenses',
        link: '/Licenses'
    },//6
]
</script>

<style lang="scss">
    .footer{
        width: 1300px;
        display: flex;
        justify-content: space-between;
        &-main{
            display: flex;
            flex-direction: column;
            &__logo{
                margin-bottom: 23px;
            }
            &__list{
                padding: 0;
                list-style-type: none;
                display: flex;
            }
            &__item{
                margin:0 10px 0 0;
                padding: 0;
            }
        }
        &-menu{
            display: flex;
            &__list{
                list-style-type: none;
                margin: 0;
                text-decoration: none;
            }
            &__item{
                color: var(--white);
                font-size: 17px;
                margin-bottom: 2px;
                line-height: 27px;
            }
        }
        &-media{
            margin-right: 219px;
        }
    }
</style>