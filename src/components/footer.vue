<script setup lang="ts">
import Logo from '@components/logo.vue'
import FacebookIcon from '@components/icon-facebook.vue'
import YoutubeIcon from '@components/icon-youtube.vue'
import TwitterIcon from '@components/icon-twitter.vue'
import PinterestIcon from '@components/icon-pinterest.vue'
import InstagramIcon from '@components/icon-instagram.vue'
import Navigation from '@components/footer-navigation.vue'
import Button from '@components/button.vue'
</script>

<template>
    <footer class="footer">
        <div class="footer__container">
            <div class="footer__section">
                <Logo text-color="#fff" />
                <div class="footer__social-networks">
                    <div class="footer__icon">
                        <FacebookIcon />
                    </div>
                    <div class="footer__icon">
                        <YoutubeIcon />
                    </div>
                    <div class="footer__icon">
                        <TwitterIcon />
                    </div>
                    <div class="footer__icon">
                        <PinterestIcon />
                    </div>
                    <div class="footer__icon">
                        <InstagramIcon />
                    </div>
                </div>
            </div>
            
            <Navigation />

            <div class="footer__section footer__section--right">
                <Button is-right>Request Invite</Button>
                <p class="footer__copyright">&copy Easybank. All Rights Reserved</p>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
@use '../assets/styles/variables';
@use '../assets/styles/mixins';

.footer {
    width: 100%;
    height: auto;
    padding-top: 4rem;
    padding-bottom: 4rem;
    background-color: variables.$color-dark-blue;

    &__container {
        @include mixins.container;
        text-align: center;

        @media screen and (min-width: variables.$screen-lg) {
            display: flex;
            flex-direction: row;
            text-align: start;
        }
    }

    &__section {
        width: auto;
        height: auto;
        margin-right: 10rem;

        &:last-child {
            margin-right: 0;
        }

        &--right {
            @media screen and (min-width: variables.$screen-lg) {
                margin-left: auto;
                text-align: end;
            }
        }
    }

    &__social-networks {
        display: flex;
        flex-direction: row;
        justify-content: center;
        width: auto;
        height: auto;
        margin-top: 3rem;
        margin-bottom: 3rem;

        @media screen and (min-width: variables.$screen-lg) {
            justify-content: flex-start;
        }
    }

    &__icon {
        width: 2.6rem;
        height: auto;
        margin-right: 1.6rem;

        &:last-child {
            margin-right: 0;
        }
    }

    &__copyright {
        font-size: 1.6rem;
        font-weight: 400;
        color: variables.$color-grayish-blue;
        margin-top: 3rem;
    }
}
</style>