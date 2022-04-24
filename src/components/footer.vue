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
      <div class="footer__section footer__section--left">
        <Logo text-color="#fff"/>
        <div class="footer__social-networks">
          <div class="footer__icon">
            <FacebookIcon/>
          </div>
          <div class="footer__icon">
            <YoutubeIcon/>
          </div>
          <div class="footer__icon">
            <TwitterIcon/>
          </div>
          <div class="footer__icon">
            <PinterestIcon/>
          </div>
          <div class="footer__icon">
            <InstagramIcon/>
          </div>
        </div>
      </div>

      <div class="footer__section footer__section--center">
        <Navigation/>
      </div>

      <div class="footer__section footer__section--right">
        <Button>Request Invite</Button>
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

  @media screen and (min-width: variables.$screen-lg) {
    padding-top: 6rem;
    padding-bottom: 6rem;
  }

  &__container {
    @include mixins.container;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 100%;
    height: auto;

    @media screen and (min-width: variables.$screen-lg) {
      flex-direction: row;
      height: 10rem;
    }
  }

  &__section {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: auto;
    height: auto;

    &:last-child {
      margin-right: 0;
    }

    @media screen and (min-width: variables.$screen-lg) {
      justify-content: space-between;
    }

    &--right {
      @media screen and (min-width: variables.$screen-lg) {
        align-items: flex-end;
        height: 100%;
        margin-left: auto;
      }
    }

    &--center {
      @media screen and (min-width: variables.$screen-lg) {
        margin-left: 10%;
      }
    }

    &--left {
      @media screen and (min-width: variables.$screen-lg) {
        align-items: flex-start;
        height: 100%;
      }
    }
  }

  &__social-networks {
    display: flex;
    flex-direction: row;
    width: auto;
    height: auto;
    margin-top: 3rem;
    margin-bottom: 3rem;

    @media screen and (min-width: variables.$screen-lg) {
      justify-content: flex-start;
      margin: 0;
    }
  }

  &__icon {
    width: auto;
    height: 2.4rem;
    margin-right: 1.6rem;

    &:last-child {
      margin-right: 0;
    }
  }

  &__copyright {
    font-size: 1.5rem;
    font-weight: 400;
    color: variables.$color-grayish-blue;
    margin-top: 3rem;
    text-align: center;
    line-height: 2.4rem;
    letter-spacing: -0.02rem;

    @media screen and (min-width: variables.$screen-lg) {
      margin: 0;
      text-align: left;
    }
  }
}
</style>