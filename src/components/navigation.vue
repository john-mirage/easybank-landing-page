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
            href=""
            v-for="(item, index) in items"
            :key="index"
        >
            {{ item }}
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

    &__link {
        display: block;
        width: auto;
        height: 100%;
        font-size: 1.6rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        line-height: 8rem;
        text-decoration: none;
        margin-right: 3rem;

        &:last-child {
            margin-right: 0;
        }
    }
}
</style>