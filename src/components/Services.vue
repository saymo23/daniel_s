<template>
  <h2 class="section__title">Services</h2><!-- /.section__title -->
  <span class="section__subtitle">What it offer</span><!-- /.section__subtitle -->

  <div class="services__container container grid">
     
    <Service v-for="s in service" :service="s" :key="s.title" />

  </div><!-- /.services__container -->

</template>

<script >
import Service from './ui/Service.vue'
export default {
  components: { Service },
  data: () => {
    return {
      service: [
        {
          title: 'Frontend <br>Developer',
          icon: 'uil-arrow',
          points: [
            'I develop the user interface.',
            'Web page development.',
            'I position your company brand.'
          ]
        },
        {
          title: 'Backend <br>Developer',
          icon: 'uil-servers',
          points: [
            'I build web server for your requirements.',
            'REST API: Nest.js and Adonis.js',
            'Configure DNS, domains & WHM/cPanel servers.'
          ]
        },
        {
          title: 'Wordpress <br>Developer',
          icon: 'uil-wordpress-simple',
          points: [
            'I develop your blog web page in Wordpress.',
            'Handcrafted Themes and optimized.',
            'I develop custom plugins'
          ]
        }
      ]
    }
  }
}
</script>

<style>

</style>
