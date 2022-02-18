<script setup lang="ts">
import Logo from '@components/logo.vue'
import FacebookIcon from '@components/icon-facebook.vue'
import YoutubeIcon from '@components/icon-youtube.vue'
import TwitterIcon from '@components/icon-twitter.vue'
import PinterestIcon from '@components/icon-pinterest.vue'
import InstagramIcon from '@components/icon-instagram.vue'
import Navigation from '@components/navigation.vue'
import Button from '@components/button.vue'
</script>

<template>
    <footer class="footer">
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
        <Navigation />
        <Button>Request Invite</Button>
        <p class="footer__copyright">&copy Easybank. All Rights Reserved</p>
    </footer>
</template>

<style lang="scss">
@use '../assets/styles/variables';

.footer {
    width: 100%;
    height: auto;
    padding: 4rem 2.4rem;
    background-color: variables.$color-dark-blue;
    text-align: center;

    &__social-networks {
        display: flex;
        flex-direction: row;
        justify-content: center;
        width: auto;
        height: auto;
        margin-top: 3rem;
        margin-bottom: 3rem;
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