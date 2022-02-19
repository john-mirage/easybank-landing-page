<script setup lang="ts">
const items = [
    "Home",
    "About",
    "Contact",
    "Blog",
    "Careers",
]
</script>

<template>
    <nav class="navigation">
        <a
            class="navigation__link"
            href="#"
            v-for="(item, index) in items"
            :key="index"
        >
            {{ item }}
            <div class="navigation__line"></div>
        </a>
    </nav>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.navigation {
    display: flex;
    flex-direction: row;
    justify-content: center;
    width: 100%;
    height: 100%;
    overflow: hidden;

    &__link {
        position: relative;
        display: block;
        width: auto;
        height: 100%;
        font-size: 1.6rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        line-height: 8rem;
        text-decoration: none;
        margin-right: 3rem;
        transition: color 300ms;

        &:last-child {
            margin-right: 0;
        }

        &:hover {
            color: variables.$color-dark-blue;
        }
    }

    &__line {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 0.4rem;
        background-image: linear-gradient(to right, variables.$color-lime-green, variables.$color-bright-cyan);
        transform: translateY(100%);
        transition: transform 300ms;

        .navigation__link:hover & {
            transform: translateY(0);
        }
    }
}
</style>