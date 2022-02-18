<script setup lang="ts">
import LatestArticle from '@components/latest-article.vue'
import CurrencyImage from '@assets/images/image-currency.jpg'
import RestaurantImage from '@assets/images/image-restaurant.jpg'
import PlaneImage from '@assets/images/image-plane.jpg'
import ConfettiImage from '@assets/images/image-confetti.jpg'

const latestArticles = [
    {
        author: "Claire Robinson",
        name: "Receive money in any currency with no fees",
        excerpt: "The world is getting smaller and we're becoming more mobile. So why should you be forced to only receive money in a single...",
        imageSrc: CurrencyImage,
        imageAlt: "Currency image",
    },
    {
        author: "Wilson Hutton",
        name: "Treat yourself without worrying about money",
        excerpt: "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you...",
        imageSrc: RestaurantImage,
        imageAlt: "Restaurant image",
    },
    {
        author: "Wilson Hutton",
        name: "Take your Easybank card wherever you go",
        excerpt: "We want you to enjoy your travels. This is why we don't charge any fees on purchases while you're abroad. We'll even show you...",
        imageSrc: PlaneImage,
        imageAlt: "Plane image",
    },
    {
        author: "Claire Robinson",
        name: "Our invite-only Beta accounts are now live!",
        excerpt: "After a lot of hard work by the whole team, we're excited to launch our closed beta. It's easy to request an invite through the site...",
        imageSrc: ConfettiImage,
        imageAlt: "Confetti image",
    },
]
</script>

<template>
    <div class="latest-articles">
        <div class="latest-articles__container">
            <h2 class="latest-articles__title">Latest Articles</h2>
            <ul class="latest-articles__list">
                <LatestArticle
                    v-for="(latestArticle, index) in latestArticles"
                    :author="latestArticle.author"
                    :name="latestArticle.name"
                    :excerpt="latestArticle.excerpt"
                    :imageSrc="latestArticle.imageSrc"
                    :imageAlt="latestArticle.imageAlt"
                    :key="index"
                />
            </ul>
        </div>
    </div>
</template>

<style lang="scss">
@use '../assets/styles/variables';
@use '../assets/styles/mixins';

.latest-articles {
    width: 100%;
    height: auto;
    padding: 8rem 2.4rem;

    &__container {
        @include mixins.container;
    }

    &__title {
        font-size: 3rem;
        font-weight: 400;
        color: variables.$color-dark-blue;
        text-align: center;
        margin-bottom: 4rem;

        @media screen and (min-width: variables.$screen-md) {
            text-align: start;
        }
    }

    &__list {
        @include mixins.grid;
    }
}
</style>