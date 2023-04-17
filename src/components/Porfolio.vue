<template>

    <h2 class="section__title">Portfolio</h2><!-- /.section__title -->
    <span class="section__subtitle">
      Most recent work
    </span><!-- /.section__subtitle -->
  
    

    <div class="portfolio__container container">
      <swiper 
      class="mySwiper"
      :navigation="true" 
      :modules="modules" 
      :autoplay="{
        delay: 2500,
        disableOnInteraction: true,
      }"
      :loop="true"
      
      >
        <swiper-slide v-for="i in items" :key="i.title" data-swiper-autoplay="2000">
          <div class="portfolio__content grid">
            <img :src="i.img" alt="#" class="portfolio__img"/>
            <div class="portfolio__data">
              <h3 class="portfolio__title">{{ i.title }}</h3><!-- /.portfolio__title -->
              <p class="portfolio__description">
                {{ i.description }}
              </p><!-- /.porfolio__description -->
              <a :href="i.link" class="button button--flex button--small portfolio__button"
                v-if="i.link">
                Demo <i class="uil uil-arrow-right button__icon"></i>
              </a><!-- /.button button--flex button--small portfolio__button -->
            </div><!-- /.portfolio__data -->
          </div><!-- /.portfolio__content grid -->
        </swiper-slide>
        
      </swiper>
      
    </div><!-- /.portfolio__container container grid -->


</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css/navigation';
import 'swiper/css/pagination';

import 'swiper/css';

import { Autoplay,Pagination, Navigation } from 'swiper';
export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup() {

    const items = [
      {
        title: 'Modern Website',
        description: 'Webiste Adaptable to all devices and animated intercations.',
        img: "1.jpg",
        link: '#'
      },
      {
        title: 'Admin: MEXICONOW CRM',
        description: 'Webiste Adaptable to all devices and animated intercations.',
        img: '1.jpg',
        link: '#'
      },
      {
        title: 'Panel: B2B Meetings System',
        description: 'Web application that allows customers to make business appointments at events organized by the company.',
        img: '1.jpg',
        link: '#'
      },
    ];
    return {
      modules: [Navigation, Pagination, Autoplay], items
    };
  },
}
</script>

<style>

</style>