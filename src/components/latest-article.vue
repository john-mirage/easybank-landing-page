<script setup lang="ts">
defineProps<{
    author: string,
    name: string,
    excerpt: string,
    imageSrc: string,
    imageAlt: string,
}>()
</script>

<template>
    <div class="latest-article">
        <img class="latest-article__image" :src="imageSrc" :alt="imageAlt">
        <div class="latest-article__body">
            <p class="latest-article__author">By {{ author }}</p>
            <h3 class="latest-article__name">{{ name }}</h3>
            <p class="latest-article__excerpt">{{ excerpt }}</p>
        </div>
    </div>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.latest-article {
    width: 100%;
    height: auto;
    border-radius: 0.6rem;
    overflow: hidden;
    background-color: variables.$color-white;
    margin-bottom: 3rem;
    box-shadow: 0 1px 2px 0 rgb(0 0 0 / 0.05);

    &__image {
        display: block;
        width: 100%;
        height: auto;
    }

    &__body {
        width: 100%;
        height: auto;
        padding: 3rem 2.4rem;
    }

    &__author {
        font-size: 1.2rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        margin-bottom: 1rem;
    }

    &__name {
        font-size: 1.8rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        margin-bottom: 1rem;
    }

    &__excerpt {
        font-size: 1.4rem;
        line-height: 2rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
    }
}
</style>