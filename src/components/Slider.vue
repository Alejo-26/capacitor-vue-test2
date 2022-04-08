<template>
  <div id="slider" class="slider-big">
    <h1>{{texto}}</h1>
    <h2>{{texto2}}</h2>
    <router-link to="/blog" class="btn-white" v-if="showBtn">Ir al blog</router-link>
    <!-- <a href="#" class="btn-white">Ir al blog</a> -->
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "Slider",
  props: ['texto','showBtn','texto2']
};
</script>

<style>
</style>
