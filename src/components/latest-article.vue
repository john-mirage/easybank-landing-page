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
        <header class="latest-article__header">
            <img class="latest-article__image" :src="imageSrc" :alt="imageAlt">
        </header>
        <div class="latest-article__body">
            <p class="latest-article__author">By {{ author }}</p>
            <a class="latest-article__name" href="#">{{ name }}</a>
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
    box-shadow: 0 1px 2px 0 rgb(0 0 0 / 0.05);

    &__header {
        position: relative;
        width: 100%;
        height: auto;
        padding-top: 56.25%;
    }

    &__image {
        position: absolute;
        top: 0;
        left: 0;
        display: block;
        width: 100%;
        height: 100%;
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
        display: block;
        font-size: 1.8rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        text-decoration: none;
        margin-bottom: 1rem;
        transition: color 150ms;

        &:hover {
            color: variables.$color-lime-green;
        }
    }

    &__excerpt {
        font-size: 1.4rem;
        line-height: 2rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
    }
}
</style>