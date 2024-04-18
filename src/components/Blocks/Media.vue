<template>
    <ul class="media__list">
        <li class="media__item" v-for="(element, i) of platforms" :key="i">
            <a :href="element.link" class="media-item__link">
            <img :src="element.img" :alt="element.name">
            </a>
        </li>
    </ul>
</template>

<script setup>
const platforms = [
    {
        name: 'Spotify',
        link: '/Spotify',
        img: 'svg/Spotify.svg',
    },
    {
        name: 'Pocket Casts',
        link: '/PocketCasts',
        img: 'svg/PocketCasts.svg',
    },
    {
        name: 'Soundcloud',
        link: '/Soundcloud',
        img: 'svg/Soundcloud.svg',
    },
    {
        name: 'Apple Podcasts',
        link: '/ApplePodcasts',
        img: 'svg/ApplePodcasts.svg',
    },
    {
        name: 'Overcast',
        link: '/Overcast',
        img: 'svg/Overcast.svg',
    },
]
</script>

<style lang="scss">
.media{
    &__list{
        margin-left: 0;
        padding-left: 0;
        display: flex;
        width: 245px;
        justify-content: space-between;
    }
    &__item{
        list-style-type: none;
    }
}
</style>