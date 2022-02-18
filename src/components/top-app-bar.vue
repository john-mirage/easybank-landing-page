<script setup lang="ts">
import Logo from '@components/logo.vue'
import IconButton from '@components/icon-button.vue'
import IconHamburger from '@components/icon-hamburger.vue'
</script>

<template>
    <header class="top-app-bar">
        <Logo text-color="#2D314D" />
        <IconButton>
            <IconHamburger />
        </IconButton>
    </header>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.top-app-bar {
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 6.4rem;
    padding-left: 2.4rem;
    padding-right: 2.4rem;
    background-color: variables.$color-white;
    box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
}
</style>
