<template >
    <div class="podcaster">
        <div class="podcaster-text">
            <div class="podcaster-text__img">
                <img src="img/vector.png" alt="vector">
            </div>
            <span class="podcaster-text__img-text">
                Meet your host
            </span>
            <span class="podcaster-text__name">
                Jacob Paulaner
            </span>
            <span class="podcaster-text__description">
                Jacob has a background in audio engineering, and has been podcasting since the early days.
            </span>
            <span class="podcaster-text__description">
                He’s here to help you level up your game by sharing everything he’s learned along the way.
            </span>
        </div>
            <img src="img/podcaster.jpg" alt="Jacob Paulaner" class="podcaster-img">
    </div>
</template>

<script setup>
</script>

<style lang="scss">
    .podcaster{
        width: 1300px;
        height: 744px;
        display: flex;
        justify-content: space-between;
        align-items: center ;
        color: var(--white);
        &-text{
            width: 590px;
            height: 448px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            &__img{
                &-vector{
                    position: absolute;
                }
                &-text{
                    color: var(--blue);
                    font-size: 18px;
                }
            }
            &__name{
                font-size: 65px;
                line-height: 79.20px;
                letter-spacing: 2.88px;
            }
            &__description{
                font-size: 22px;
                color: var(--lightGrey);
            }
        }
        &-img{
            width: 650px;
            height: 743px;
            border-radius: 15px;
        }
    }
</style>