<script setup lang="ts">
defineProps<{
  isLeft?: boolean,
  isRight?: boolean,
}>()
</script>

<template>
  <button
      class="button"
      :class="{
        'button--left': isLeft,
        'button--right': isRight,
      }"
  >
    <slot/>
    <div class="button__overlay"></div>
  </button>
</template>

<style lang="scss">
@use '../assets/styles/variables.scss';

.button {
  position: relative;
  display: block;
  height: 4.4rem;
  overflow: hidden;
  padding-left: 3.2rem;
  padding-right: 3.2rem;
  background-image: linear-gradient(to right, variables.$color-lime-green, variables.$color-bright-cyan);
  color: variables.$color-white;
  font-size: 1.4rem;
  font-weight: 700;
  border-radius: 9999px;
  border: none;
  outline: none;
  cursor: pointer;

  &--right {
    margin-left: auto;
  }

  &__overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(255, 255, 255, 0.3);
    opacity: 0;
    transition: opacity 150ms;

    .button:hover & {
      opacity: 1;
    }
  }
}
</style>