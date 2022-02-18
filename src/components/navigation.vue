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
    <nav class="navigation">
        <a
            class="navigation__item"
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

.navigation {
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
    width: 100%;
    height: auto;
    margin-bottom: 2rem;

    &__item {
        font-size: 1.6rem;
        font-weight: 400;
        text-decoration: none;
        color: variables.$color-white;
        padding-top: 1rem;
        padding-bottom: 1rem;
    }
}
</style>