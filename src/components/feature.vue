<script setup lang="ts">
defineProps<{
    name: string,
    description: string,
    iconSrc: string,
    iconAlt: string,
}>()
</script>

<template>
    <section class="feature">
        <img class="feature__logo" :src="iconSrc" :alt="iconAlt">
        <h3 class="feature__name">{{ name }}</h3>
        <p class="feature__description">{{ description }}</p>
    </section>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.feature {
    width: 100%;
    height: auto;
    margin-bottom: 4rem;
    text-align: center;

    @media screen and (min-width: variables.$screen-md) {
        text-align: start;
        margin-bottom: 0;
    }

    &__logo {
        margin-bottom: 3rem;
    }

    &__name {
        font-size: 2.4rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        line-height: 3rem;
        margin-bottom: 2rem;
    }

    &__description {
        max-width: 30rem;
        margin-left: auto;
        margin-right: auto;
        font-size: 1.6rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        line-height: 2.4rem;

        @media screen and (min-width: variables.$screen-md) {
            max-width: unset;
            margin: 0;
        }
    }
}
</style>