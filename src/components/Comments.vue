<template>
    <div class="comments" >
        <div class="comment" v-for="(comment, i) of comments" :key="i">
            <div class="comment-rating">
                <img src="svg/star.svg" :alt="index" v-for="index in comment.rate" :key="index" class="comment-rating__item">
            </div>
            <div class="comment-text">
                {{ comment.text }}
            </div>
            <div class="comment-user">
                {{ comment.user }}
            </div>
        </div>
    </div>
</template>

<script setup>
const comments = [
        {
            rate: 5,
            text: 'I can’t recommend this podcast enough',
            user: 'Betty Lacey'
        },
        {
            rate: 4,
            text: 'Jacob is the best in the business',
            user: 'Adam Driver'
        },
        {
            rate: 5,
            text: 'A wealth of audio knowledge',
            user: 'Marcus Brown'
        },
        {
            rate: 4,
            text: 'Every episode is a gem!',
            user: 'Jessica Knowl'
        },
        {
            rate: 3,
            text: 'Whoa whoa, let me take some notes!',
            user: 'Scott Adams'
        },
        {
            rate: 5,
            text: 'I’ve upped my game considerably since I started listening',
            user: 'Steven Blast'
        },
    ]
</script>
<style lang="scss">
.comments{
    display: grid;
    grid-template-columns:  repeat(3, 423px);
    grid-template-rows: repeat(2, 364px);
    grid-gap: 15px;
    margin-bottom: 200px;
}
.comment{
    color: var(--white);
    border-radius: 32px;
    background-color: var(--black);
    padding: 50px;
    &-rating{
        &__item{
            padding-right: 5px;
            margin-bottom: 21px;
        }
    }
    &-text{
        font-size: 36px;
        line-height: 43.20px;
        margin-bottom: 19px;
    }
    &-user{
        font-size: 23px;
        color: var(--lightGrey);
    }
}
</style>