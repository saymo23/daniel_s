<template>
  <div class="skills__data" v-for="s in skills"  v-bind:key="s.title">
    <div class="skills__titles">
      <h3 class="skills__name">{{ s.title }}</h3><!-- /.skills__name -->
      <span class="skills__subtitle">{{ s.subtitle }}</span><!-- /.skills__subtitle -->
    </div><!-- /.skills__title -->
  </div>
</template>

<script>

export default {
  props: [
    'skills',
  ]
};

</script>

<style>

</style>