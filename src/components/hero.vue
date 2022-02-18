<script setup lang="ts">
import Button from '@components/button.vue'
</script>

<template>
    <div class="hero">
        <div class="hero__background"></div>
        <div class="hero__mockups"></div>
        <div class="hero__container">
            <section class="hero__info">
                <h1 class="hero__title">Next generation digital banking</h1>
                <p class="hero__description">Take your financial life online. Your Easybank account will be a one-stop-shop for spending, saving, budgeting, investing, and much more.</p>
                <Button>Request Invite</Button>
            </section>
        </div>
    </div>
</template>

<style lang="scss">
@use '../assets/styles/variables';
@use '../assets/styles/mixins';

.hero {
    position: relative;
    width: 100%;
    height: auto;
    margin-top: 6.4rem;
    margin-bottom: 8rem;
    padding-top: 85%;

    @media screen and (min-width: variables.$screen-lg) {
        height: 60rem;
        padding-top: 0;
        margin-top: 8rem;
        margin-bottom: 0;
    }

    &__background {
        position: absolute;
        z-index: 10;
        top: 0;
        left: 0;
        width: 100%;
        height: auto;
        padding-top: 90%;
        background-image: url(src/assets/images/bg-intro-mobile.svg);
        background-repeat: no-repeat;
        background-size: 100% 100%;
        pointer-events: none;

        @media screen and (min-width: variables.$screen-lg) {
            left: 50%;
            width: 50%;
            height: 100%;
            padding-top: 0;
            background-position: top -30rem left -8rem;
            background-size: auto 200%;
            background-image: url(src/assets/images/bg-intro-desktop.svg);
        }
    }

    &__mockups {
        position: absolute;
        z-index: 20;
        top: 0;
        left: 0;
        width: 100%;
        height: auto;
        padding-top: 78%;
        background-image: url(src/assets/images/image-mockups.png);
        background-repeat: no-repeat;
        background-size: 90% auto;
        background-position: bottom center;

        @media screen and (min-width: variables.$screen-lg) {
            left: calc(50% + 10rem);
            width: calc(50% - 10rem);
            height: 125%;
            padding-top: 0;
            background-size: 70rem auto;
            background-position: bottom left;
        }
    }

    &__container {
        @include mixins.container;
        display: flex;
        flex-direction: column;
        justify-content: center;
        height: 100%;
    }

    &__info {
        width: 100%;
        height: auto;
        text-align: center;

        @media screen and (min-width: variables.$screen-lg) {
            width: 50%;
            text-align: start;
        }
    }

    &__title {
        width: 100%;
        height: auto;
        font-size: 4rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        margin-bottom: 2rem;

        @media screen and (min-width: variables.$screen-lg) {
            width: 40rem;
        }
    }

    &__description {
        font-size: 1.4rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        line-height: 2rem;
        margin-bottom: 3rem;

        @media screen and (min-width: variables.$screen-lg) {
            width: 40rem;
        }
    }
}
</style>