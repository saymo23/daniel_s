<template>
  <div class="home__container container grid">
    <div class="home__content grid">
      <div class="home__social">
        <a v-for="s in socials" href="#" class="home__social-icon" v-bind:key="s.url">
          <i class="uil" :class="s.icon"></i>
        </a><!-- /.home__social-icon -->
      </div><!-- /.home__social -->

      <div class="home__img">
        <Blob />
      </div><!-- /.home__img -->

      <div class="home__data">
        <h1 class="home__title">Hi, I'm Daniel Santarriaga</h1>
        <h3 class="home__subtitle">and I'm Web Developer</h3>
        <p class="home__description">
          High level experience in web development and mobile applications.
        </p><!-- /.home__description -->
        <a href="#contact" class="button button--flex">
          Contact Me <i class="uil uil-message"></i>
        </a><!-- /.button button--flex -->
      </div><!-- /.home__data -->
    </div><!-- /.home__content grid -->

    <div class="home__scroll">
      <a href="#abaout" class="home__scroll-button button--flex">
        <i class="uil uil-mouse-alt home__scroll-mouse"></i>
        <span class="home__scroll-name">Scroll down</span>
        <i class="uil uil-arrow-down home__scroll-arrow"></i>
      </a><!-- /.home__scroll-button button--flex -->
    </div><!-- /.home__scroll -->

  </div><!-- /.home__container container grid -->
</template>

<script setup>
import Blob from "./icons/blob.vue";
  const socials = [
    {
      url: '#twitter',
      icon: 'uil-twitter-alt'
    },
    {
      url: '#github',
      icon: 'uil-github-alt'
    }
  ]

</script>