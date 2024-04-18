<template>
    <button class="button">
        <slot />
    </button>
</template>

<script setup>

</script>

<style lang="scss">
    .button{
        padding: 12px 15px 12px 20px;
        background-color: var(--blue);
        color: var(--white);
        text-align: center;
        font-size: 17px;
        border-radius: 6px;
        border: none;
        cursor: pointer;
        &:hover{
            opacity: 0.30;
        }
    }
</style>