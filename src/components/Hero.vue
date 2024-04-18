<template>
    <div class="hero">
            <img src="img/hero.jpg" alt="Hero" class="hero__img">
            <img src="svg/hero-angle.svg" alt="hero-angle" class="hero__img-angle">
        <div class="hero-info">
            <p class="hero-info__text">Take your podcast to the <br>
                <span class="hero-info__text-next">
                <img src="svg/underline.svg" alt="underline" class="hero-info__text-next__underline"> 
                     next
                </span> 
                <span class="hero-info__text-level"> level </span>
            </p>
            <div class="hero-info-platforms">
                <p class="hero-info-platforms__text">Listen on</p>
                <Media />
            </div>
        </div>
    </div>
</template>

<script setup>
import Media from './Blocks/Media.vue'
</script>

<style lang="scss">
    .hero{
        padding: 40px 50px 0 50px;
        display: flex;
        align-items: center;
        &__img{
            border-radius: 15px;
            &-angle{
                position: relative;
                right: 676px;
                bottom: 425px;
            }
        }
        &-info{
            height: 610px;
            width: 530px;
            padding: 0 50px;
            &__text{
                color: var(--white);
                font-size: 70px;
                width: 526px;
                line-height: 88px;
                font-weight: 400;
                letter-spacing: 3.20px;
                &-next {
                    &__underline{
                        position: absolute;
                        width: 160px;
                    }
                }
                &-level{
                    font-weight: 700;
                }
            }
            &-platforms{
                display: flex;
                flex-direction: column;
                color: var(--white);
                font-size: 15px;
                width: 289px;
                height: 72px;
                margin-top:90px;
                &__text{
                    margin-bottom: 16px;
                }
            }
        }
    }
</style>