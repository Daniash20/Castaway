<template>
    <header class="header">
        <div class="header-logo">
            <img src="svg/logo.svg" alt="Logo">
        </div>
        <nav class="header-menu">
            <ul class="header-menu__list">
                <li v-for="(element, i) of nav" :key="i" class="header-menu__item">
                    <a href="/" class="header-menu__link">
                        {{ element.name }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script setup>
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
</script>

<style lang="scss">
.header {
    height: 119px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    &-menu {
        width: 403px;
        &__list{
            display: flex;
        }
        &__item{
            list-style-type: none;
            padding-right: 20px;
            margin: 0;
        }
        &__link {
            color: var(--white);
            text-decoration: none;
            &:hover {
                color: #118DA8;
            }
        }
    }
}
</style>