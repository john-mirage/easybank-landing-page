<script setup lang="ts">
defineProps<{
  closeDrawer: () => void,
}>()
const items = [
  "Home",
  "About",
  "Contact",
  "Blog",
  "Careers",
]
</script>

<template>
  <aside class="drawer">
    <nav class="drawer__navigation">
      <a
          class="drawer__link"
          href="#"
          v-for="(item, index) in items"
          :key="index"
      >
        {{ item }}
      </a>
    </nav>
    <div class="drawer__overlay" @click="closeDrawer"></div>
  </aside>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.drawer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  transform: translateY(100%);
  width: 100%;
  height: calc(100vh - 6.4rem);
  padding-top: 2.4rem;
  padding-left: 2.4rem;
  padding-right: 2.4rem;

  @media screen and (min-width: variables.$screen-lg) {
    display: none;
  }

  &__navigation {
    position: relative;
    z-index: 50;
    width: 100%;
    max-width: 32.7rem;
    height: auto;
    margin-left: auto;
    margin-right: auto;
    background-color: variables.$color-white;
    border-radius: 0.4rem;
    text-align: center;
    padding: 2.4rem;
  }

  &__link {
    display: block;
    text-decoration: none;
    font-size: 1.8rem;
    font-weight: 400;
    color: variables.$color-dark-blue;
    margin-bottom: 2.4rem;

    &:last-child {
      margin-bottom: 0;
    }
  }

  &__overlay {
    position: absolute;
    z-index: 40;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(45, 49, 77, 0.9), rgba(45, 49, 77, 0));
    cursor: pointer;
  }
}
</style>