<template>
    <div class="subscribe">
        <div class="subscribe-text">
            <div class="subscribe-text__first">
                <span>Email Newletter</span>
            </div>
            <div class="subscribe-text__second">
                <span>Subscribe for updates</span>
            </div>
        </div>
        <form class="subscribe-form">
            <input type="text" placeholder="Name">
            <input type="email" placeholder="Email">
            <div class="subscribe-form__button">
                <uiButton type="submit">Submit</uiButton>
            </div>
        </form>
    </div>
    <img src="img/subscribe-angle.png" alt="angle" class="subscribe__angle">
</template>
<script setup>
import uiButton from '@/components/UI/Button.vue'
</script>
<style lang="scss">
    .subscribe{
        margin: 200px 0;
        padding: 60px;
        display: flex;
        justify-content: space-between;
        background: var(--black);
        width: 1300px;
        height: 387px;
        border-radius:32px;
        align-items: center;
        &-text{
            &__first{
                color: var(--blue);
                font-size: 18px;
            }
            &__second{
                color: var(--white);
                font-size: 72px;
                width:431px;
                letter-spacing: 2.88px;
            }
        }
        &-form{
            display: flex;
            flex-direction: column;
            input{
                width: 522px;
                padding: 26px  0 27px 19px;
                height: 82px;
                color: var(--lightGrey);
                font-size: 24px;
                background-color: var(--grey);
                border: none;
                border-radius: 8px;
                margin-bottom: 20px;
            }
            &__button{
                color:var(--lightGrey);
            }
        }
        &__angle{
            position: relative;
            bottom: 250px;
            right: 30px;
        }
    }
</style>