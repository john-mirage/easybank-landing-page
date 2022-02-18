<script setup lang="ts">
import Button from '@components/button.vue'
import mockupsImage from '@assets/images/image-mockups.png'
</script>

<template>
    <div class="hero">
        <div class="hero__illustration"></div>
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

    &__illustration {
        display: block;
        width: 100%;
        height: auto;
        padding-bottom: 100%;
        background-image:
            url(src/assets/images/image-mockups.png),
            url(src/assets/images/bg-intro-mobile.svg);
        background-repeat: no-repeat;
        background-size: 100% auto, 100% 100%;
        background-position: 0% 158%, 0% 0%;
    }

    &__info {
        width: 100%;
        height: auto;
        padding-left: 2.4rem;
        padding-right: 2.4rem;
        text-align: center;
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