<script setup lang="ts">
defineProps<{
  name: string,
  description: string,
  iconSrc: string,
  iconAlt: string,
}>()
</script>

<template>
  <section class="feature">
    <img class="feature__logo" :src="iconSrc" :alt="iconAlt">
    <h3 class="feature__name">{{ name }}</h3>
    <p class="feature__description">{{ description }}</p>
  </section>
</template>

<style lang="scss">
@use '../assets/styles/variables';
@use '../assets/styles/mixins';

.feature {
  width: 100%;
  height: auto;
  margin-bottom: 4rem;
  text-align: center;

  @media screen and (min-width: variables.$screen-md) {
    text-align: start;
    margin-bottom: 0;
  }

  &__logo {
    margin-bottom: 3rem;
  }

  &__name {
    @include mixins.text-sub-heading;
    margin-bottom: 2rem;
  }

  &__description {
    @include mixins.text-body;
    max-width: 30rem;
    margin-left: auto;
    margin-right: auto;

    @media screen and (min-width: variables.$screen-md) {
      max-width: unset;
      margin: 0;
    }
  }
}
</style>