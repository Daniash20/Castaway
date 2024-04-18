<template>
  <div class="container">
    <VHeader />
    <VHero />
    <Episodes />
    <Podcaster />
    <Subscribe />
    <Comments />
    <VFooter />
  </div>
</template>

<script setup>
import VHeader from '@/components/Header.vue';
import VHero from '@/components/Hero.vue';
import Episodes from "@/components/Episodes.vue";
import Podcaster from './components/Podcaster.vue';
import Subscribe from './components/Subscribe.vue';
import Comments from './components/Comments.vue';
import VFooter from './components/Footer.vue'
</script>

<style lang ="scss">
@import '@/assets/styles/global.scss';
</style>
