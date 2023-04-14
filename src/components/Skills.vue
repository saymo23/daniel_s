<template>
  <h2 class="section__title">Skills</h2><!-- /.sections__title -->
  <span class="section__subtitle">My technical Skills</span><!-- /.section__subtitle -->
  <div class="skills__container container grid">
    <div>
      
      <SkillsSection v-for="ss in skills_sections" v-bind:key="ss.title"
        :title="ss.title"
        :subtitle="ss.subtitle"
        :icon="ss.icon"
        :skills="ss.skills"
      />
      

    </div>
  </div><!-- /.skills__container container grid -->
</template>

<script setup>

import { ref } from "vue"

import SkillsSection from "./ui/SkillsSection.vue";
 
const skills_frontend = [

  {
    'title': 'HTML, CSS, Web Design',
    'subtitle': 'HTML 5, Animate Transitions, Frontend Designer'
  },
  {
    'title': 'Javascript',
    'subtitle': 'Mid-level Skills'
  },
  {
    'title': 'Vuejs',
    'subtitle': 'v2 & v3, Nuxt.js & Vuetify Design'
  },
  {
    'title': 'React',
    'subtitle': 'Low-level Skills'
  }
  
]

const skills_backend = [
  {
    'title': 'PHP',
    'subtitle': 'Mid-level, Wordpress Expert, Laravel Api Rest, Codeigniter Framework'
  },
  {
    'title': 'Node.js',
    'subtitle': 'Mid-level, Nest.js & Adonis.Js Frameworks'
  },
  {
    'title': 'Servers',
    'subtitle': 'cPanel Configurations & AWS low-level, Domains & DNS configurations'
  },
]


const skills_sections = ref([
  {
    'title': 'Frontend developer',
    'subtitle': 'More than 10 years',
    'icon': 'uil-brackets-curly',
    'skills': skills_frontend
  },
  {
    'title': 'Backend developer',
    'subtitle': 'More than 8 years',
    'icon': 'uil-server',
    'skills': skills_backend
  },

])

</script>

<style>

</style>