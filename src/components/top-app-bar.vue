<script setup lang="ts">
import Logo from '@components/logo.vue'
import IconButton from '@components/icon-button.vue'
import IconHamburger from '@components/icon-hamburger.vue'
</script>

<template>
    <header class="top-app-bar">
        <div class="top-app-bar__container">
            <Logo text-color="#2D314D" />
            <IconButton>
                <IconHamburger />
            </IconButton>
        </div>
    </header>
</template>

<style lang="scss">
@use '../assets/styles/variables';
@use '../assets/styles/mixins';

.top-app-bar {
    position: fixed;
    z-index: 100;
    top: 0;
    left: 0;
    width: 100%;
    height: 6.4rem;
    background-color: variables.$color-white;
    box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);

    &__container {
        @include mixins.container;
        display: flex;
        height: 100%;
        justify-content: space-between;
        align-items: center;
    }
}
</style>
