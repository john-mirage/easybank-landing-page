<script setup lang="ts">
import Button from '@components/button.vue'
import mockupsImage from '@assets/images/image-mockups.png'
</script>

<template>
    <div class="hero">
        <div class="hero__illustration">
            <img class="hero__mockups" :src="mockupsImage" alt="Application mockups image">
        </div>
        <section class="hero__info">
            <h1 class="hero__title">Next generation digital banking</h1>
            <p class="hero__description">Take your financial life online. Your Easybank account will be a one-stop-shop for spending, saving, budgeting, investing, and much more.</p>
            <Button>Request Invite</Button>
        </section>
    </div>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.hero {
    width: 100%;
    height: auto;
    padding-top: 6.4rem;
    padding-bottom: 8rem;

    @media screen and (min-width: variables.$screen-lg) {
        display: flex;
        flex-direction: row;
        padding-bottom: 0;
    }

    &__illustration {
        position: relative;
        z-index: 10;
        display: block;
        width: 100%;
        height: auto;
        padding-bottom: 100%;
        background-image: url(src/assets/images/bg-intro-mobile.svg);
        background-repeat: no-repeat;
        background-size: 100% 100%;

        @media screen and (min-width: variables.$screen-lg) {
            order: 2;
            padding-bottom: 56.25%;
        }
    }

    &__mockups {
        position: absolute;
        top: 0;
        left: 0;
        display: block;
        width: 100%;
        height: 100%;
        transform: translateY(-15%);

        @media screen and (min-width: variables.$screen-lg) {
            transform: translateY(15%);
        }
    }

    &__info {
        width: 100%;
        height: auto;
        padding-left: 2.4rem;
        padding-right: 2.4rem;
        text-align: center;

        @media screen and (min-width: variables.$screen-lg) {
            order: 1;
        }
    }

    &__title {
        width: 100%;
        height: auto;
        text-align: center;
        font-size: 4rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        margin-bottom: 2rem;
    }

    &__description {
        font-size: 1.4rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        line-height: 2rem;
        margin-bottom: 3rem;
    }
}
</style>