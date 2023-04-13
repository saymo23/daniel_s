<template>
  <div class="skills__content" :class="{ 'skills__close': is_active_skill }">
    <div class="skills__header "  @click="toggleOpen()">
      <i class="uil skills__icon" :class="icon"></i><!-- /.uil skills__icon -->

      <div class="skills__text">
        <h2 class="skills__titles">{{ title }}</h2><!-- /.skills__title -->
        <span class="skills__subtitle">{{ subtitle }}</span><!-- /.skills__sbutitle -->
      </div>

      <i class="uil uil-angle-down skills__arrow"></i><!-- /.uil uil-angle-down skills__arrow -->
    </div><!-- /.skills__header -->
    <div class="skills__list grid" :class="{ 'height-transition': true, 'open': state.isOpen }">
      <SkillsData :skills="skills"/>
    </div><!-- /.skills__list grid -->

  </div><!-- /.skills__content -->
</template>

<script>
import { reactive } from 'vue';
import SkillsData from './SkillsData.vue';

export default {
    props: ["title", "subtitle", "icon", "skills"],
    components: { SkillsData },
    methods:{
      toggleSkill(){
        this.is_active_skill = !this.is_active_skill
        console.log(this.is_active_skill);
      }
    },
    data(){
      return {
        is_active_skill: true
      }
    },
    setup(){
      const state = reactive({
        isOpen : false
      });

      const toggleOpen = () => {
        state.isOpen = !state.isOpen
      }
      return { state, toggleOpen }
    }
}
</script>

<style>

</style>