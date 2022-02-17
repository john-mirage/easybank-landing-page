<template>
    <button class="icon-button">
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
    margin-left: 0;
    margin-right: -1.2rem;
    padding: 0;
    border-radius: 50%;
    outline: none;
    border: none;
    background-color: transparent;

    &__icon {
        display: block;
        margin: auto;
    }
}
</style>