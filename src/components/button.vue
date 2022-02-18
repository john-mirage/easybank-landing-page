<script setup lang="ts">
</script>

<template>
    <button class="button">
        <slot />
    </button>
</template>

<style lang="scss">
@use '../assets/styles/variables.scss';

.button {
    padding: 1.4rem 4rem;
    background-image: linear-gradient(to right, variables.$color-lime-green, variables.$color-bright-cyan);
    color: variables.$color-white;
    font-size: 1.6rem;
    font-weight: 700;
    border-radius: 9999px;
    border: none;
    outline: none;
}
</style>