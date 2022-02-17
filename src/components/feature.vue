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

    &__logo {
        margin-bottom: 2rem;
    }

    &__name {
        font-size: 2rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        margin-bottom: 2rem;
    }

    &__description {
        font-size: 1.4rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        line-height: 2rem;
    }
}
</style>