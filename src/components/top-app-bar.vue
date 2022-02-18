<script setup lang="ts">
import Logo from '@components/logo.vue'
import IconButton from '@components/icon-button.vue'
import IconHamburger from '@components/icon-hamburger.vue'
import Button from '@components/button.vue';
</script>

<template>
    <header class="top-app-bar">
        <div class="top-app-bar__container">
            <div class="top-app-bar__section">
                <Logo text-color="#2D314D" />
            </div>
            <div class="top-app-bar__section top-app-bar__section--mobile">
                <IconButton class="top-app-bar__icon-button">
                    <IconHamburger />
                </IconButton>
            </div>
            <div class="top-app-bar__section top-app-bar__section--desktop">
                <Button class="top-app-bar__button">Request Invite</Button>
            </div>
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

    @media screen and (min-width: variables.$screen-lg) {
        height: 8rem;
    }

    &__container {
        @include mixins.container;
        display: flex;
        height: 100%;
        justify-content: flex-start;
        align-items: center;
    }

    &__section {
        flex: 1 1 auto;

        &--mobile {
            display: block;

            @media screen and (min-width: variables.$screen-lg) {
                display: none;
            }
        }

        &--desktop {
            display: none;

            @media screen and (min-width: variables.$screen-lg) {
                display: block;
            }
        }
    }

    &__icon-button {
        display: block;
        margin-left: auto;
    }

    &__button {
        display: block;
        margin-left: auto;
    }
}
</style>
