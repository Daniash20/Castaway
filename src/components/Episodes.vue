<template>
    <div class="episodes">
        <div class="episodes-container">
            <h2 class="episodes__title">Latest episodes</h2>
            <uiButton>View all episodes </uiButton>
        </div>
        <div class="episodes-list" v-for="(element, i) of episodes" :key="i">
            <img class="episodes-list__img" :src="element.img" :alt="name">
            <div class="episodes-list-text">
                <div class="episodes-list-text__theme">
                    <span class="episodes-list-text__theme-text">{{ element.theme }}</span>
                </div>
                <div class="episodes-list-text__number">
                    <span>Episode {{ element.number }}</span>
                </div>
                <div class="episodes-list-text__name">
                    <span class="eposodes-list-text__name-text">{{ element.name }}</span>
                </div>
                <span class="episodes-list-text__description">
                    {{ element.description }}
                </span>
                <div class="episodes-list-text__button">
                    <uiButton> View episodes details</uiButton>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import uiButton from '@/components/UI/Button.vue'
const episodes = [
    {
        img: 'img/3rd.jpg',
        theme: 'Gear',
        number: '3',
        name: 'Should you get outboard audio gear?',
        description: 'Is hardware really worth it when it comes to podcasting? The answer is...it depends. Here’s our reasons on why you might want to consider picking something up.',
    },
    {
        img: 'img/2nd.jpg',
        theme: 'Tips & Tricks',
        number: '2',
        name: 'Mic tricks to take you to the next level',
        description: 'Stop rolling with those default settings on your mic. These small tweaks will take you from sounding good to great.',
    },
    {
        img: 'img/1st.jpg',
        theme: 'Gear',
        number: '1',
        name: 'The best microphone under $200',
        description: 'With so many microphones on the market, how are you supposed to know what’s the best? Take a look at our top picks.',
    },
]
</script>

<style lang="scss">
    .episodes{
        color: var(--white);
        margin-top: 100px;
        &-container{
            margin-bottom: 60px;
            height: 100px;
            width:1300px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        &__title{
            font-weight: 400;
            font-size: 64px;
            letter-spacing: 2.88px;
        }
        &-list{
            font-weight: 400;
            width: 1300px;
            height: 512px;
            padding: 40px;
            border-radius: 32px;
            margin-bottom: 60px;
            display: flex;
            background-color: var(--black);
            
            &__img{
                width: 389px;
                height: 432px;
            }
            &-text{
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                width: 778px;
                margin-left: 60px;
                &__theme{
                    margin:7px 0 48px 0;
                    &-text{
                    line-height: 27px;
                    padding: 0 16px;
                    border-radius: 6px;
                    font-size: 18px;
                    background-color: var(--grey);
                    }
                }
                &__number{
                    color: var(--blue); 
                    line-height: 27px;
                }
                &__name{
                    line-height: 70.40px;
                    letter-spacing: 2.56px;   
                    font-size: 64px;
                    letter-spacing: 2.56px;
                }
                &__description{
                    line-height: 33px;
                    font-size: 22px;
                    color: var(--lightGrey);
                }
            }
        }
    }
</style>