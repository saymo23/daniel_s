<template>
  <header class="header" id="header">
    <nav class="nav container">
      <a href="" class="nav__logo"> Daniel Santarriaga </a><!-- /.nav__logo -->

      <div class="nav__menu" :class="{'nav__active': isNavMenuActive}" id="nav-menu">
        <ul class="nav__list grid">
          <li class="nav__item" v-for="i in menu" v-bind:key="i.url">
            <a href="#" class="nav__link" @click="goNext()">
              <i class="uil nav__icon" :class="i.icon"></i> {{ i.title }}
            </a><!-- /.nav__link -->
          </li><!-- /.nav__item -->
          <i class="uil uil-times nav__close" id="nav-close" @click="toggle_menu()"></i>
        </ul><!-- /.nav__list grid -->
      </div><!-- /#nav-menu.nav__menu -->
      <div class="nav__btns">
        <div class="nav__toggle" id="nav-toggle" @click="toggle_menu()">
          <i class="uil uil-apps "></i>
        </div><!-- /#nav-toggle.nav__toggle -->
      </div><!-- /.nav__btns -->
    </nav><!-- /.nav -->
  </header>

  <main class="main">
    <!--==================== HOME ====================-->
    <section class="home section" id="home">
      <Home/>
      
    </section>

    <!--==================== ABOUT ====================-->
    <section class="about section" id="about">
        
    </section>

    <!--==================== SKILLS ====================-->
    <section class="skills section" id="skills">

    </section>

    <!--==================== QUALIFICATION ====================-->
    <section class="qualification section">

    </section>

    <!--==================== SERVICES ====================-->
    <section class="services section" id="services">
        
    </section>

    <!--==================== PORTFOLIO ====================-->
    <section class="portfolio section" id="portfolio">
        
    </section>

    <!--==================== PROJECT IN MIND ====================-->
    <section class="project section">

    </section>

    <!--==================== TESTIMONIAL ====================-->
    <section class="testimonial section">
        
    </section>

    <!--==================== CONTACT ME ====================-->
    <section class="contact section" id="contact">

    </section>
  </main>

  <!--==================== FOOTER ====================-->
  <footer class="footer">
    
  </footer>
  
</template>

<script setup>
import Home from "./components/Home.vue";
import { ref } from 'vue'

let isNavMenuActive = ref(false);

const menu = [
  {
    link: '#',
    title: 'Home',
    icon: 'uil-estate'
  },
  {
    link: '#',
    title: 'About',
    icon: 'uil-user'
  },
  {
    link: '#',
    title: 'Skills',
    icon: 'uil-file-alt'
  },
  {
    link: '#',
    title: 'Services',
    icon: 'uil-briefcase'
  },
  {
    link: '#',
    title: 'Portfolio',
    icon: 'uil-scenery'
  },
  {
    link: '#',
    title: 'Contact',
    icon: 'uil-message'
  },
]

const toggle_menu = () => {
  isNavMenuActive.value = !isNavMenuActive.value;
}

const goNext = () => {
  toggle_menu();
}

</script>

<style scoped>

</style>
