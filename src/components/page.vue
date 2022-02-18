<script setup lang="ts">
import TopAppBar from '@components/top-app-bar.vue'
import Hero from '@components/hero.vue'
import Features from '@components/features.vue'
import LatestArticles from '@components/latest-articles.vue'
import Footer from '@components/footer.vue'
</script>

<template>
    <TopAppBar />
    <Hero />
    <Features />
    <LatestArticles />
    <Footer />
</template>

<style lang="scss">
@use '../assets/styles/variables';

#app {
    background-color: variables.$color-very-light-gray;
}
</style>
