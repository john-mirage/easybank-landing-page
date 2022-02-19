<script setup lang="ts">
const items = [
    "About Us",
    "Contact",
    "Blog",
    "Careers",
    "Support",
    "Privacy Policy",
]
</script>

<template>
    <nav class="footer-navigation">
        <a
            class="footer-navigation__item"
            v-for="(item, index) in items"
            :key="index"
            href="#"
        >
            {{ item }}
        </a>
    </nav>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.footer-navigation {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    width: auto;
    height: auto;
    margin-bottom: 3rem;

    @media screen and (min-width: variables.$screen-lg) {
        grid-template-columns: repeat(2, 1fr);
    }

    &__item {
        font-size: 1.6rem;
        font-weight: 400;
        text-decoration: none;
        color: variables.$color-white;
        text-align: center;
        transition: color 150ms;

        &:hover {
            color: variables.$color-lime-green;
        }
    }
}
</style>