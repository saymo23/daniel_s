<template>
  <div class="services__content">
    <div>
      <i class="uil services__icon" :class="service.icon"></i>
      <h3 class="services__title" v-html="service.title"></h3>
    </div>
      
    <span class="button button--flex button--small button--link services__button" @click="showModal()">
      View More
      <i class="uil uil-arrow-right service__icon button__icon"></i>
    </span><!-- /.button button--flex button--small button--link services__button -->
    
    <div class="services__modal " :class="{'services__modal-active': state.is_modal_active}">
      <div class="services__modal-content">
        <h4 class="services__modal-title" v-html="service.title"></h4>
        <i class="uil uil-times services__modal-close" @click="showModal()"></i><!-- /.uil uil-times services__modal-close -->
        <ul class="services__modal-services grid">
          <li v-for="p in service.points" :key="p" class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i> 
            <p >{{ p }}</p>
          </li><!-- /.services__modal-service -->
        </ul><!-- /.services__modal-services grid -->
      </div><!-- /.services__modal-content -->
    </div><!-- /.services__modal -->

  </div><!-- /.services__content -->
</template>

<script>
import { reactive } from 'vue';
export default {
  props: ['service'],
  data: () => {
    return {
      is_modal_active: false
    }
  },
  setup(){
    const state = reactive({
      is_modal_active : false
    });

    const showModal = () => {
      console.log(state.is_modal_active);
      state.is_modal_active = !state.is_modal_active
    }
    return { state, showModal }
  }
}
</script>

<style>

</style>