<template>
  <div class="general">
    <Slider
    texto="Prosumer list"></Slider>
    <div class="center">
      <section id="content">
        <h2 class="subheader">Prosumer list</h2>
       <!-- <button @click="redirigirAlBlog()">Redirigir</button> -->
      </section>
      <SideBar></SideBar>
      <div class="clearfix"></div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import Slider from "./Slider";
import SideBar from "./SideBar.vue";

export default {
  name: "Pagina",
  components:{
    Slider,
    SideBar
  },
  methods: {
    redirigirAlBlog() {
      this.$router.push("./blog");
    },
  },
};
</script>