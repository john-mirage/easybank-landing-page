<script setup lang="ts">
defineProps<{
    isLeft?: boolean,
    isRight?: boolean,
}>()
</script>

<template>
    <button
        class="icon-button"
        :class="{
            'icon-button--left': isLeft,
            'icon-button--right': isRight,
        }"
    >
        <span class="icon-button__icon">
            <slot />
        </span>
    </button>
</template>

<style lang="scss">
.icon-button {
    display: flex;
    width: 4.8rem;
    height: 4.8rem;
    padding: 0;
    border-radius: 50%;
    outline: none;
    border: none;
    background-color: transparent;

    &--right {
        margin-left: auto;
        margin-right: -1.2rem;
    }

    &--left {
        margin-left: -1.2rem;
    }

    &__icon {
        display: block;
        margin: auto;
    }
}
</style>