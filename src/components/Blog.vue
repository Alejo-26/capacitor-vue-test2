<template>
  <div class="general">
    <Slider 
    texto="Settings"></Slider>
    <div class="center">
        
      <section id="content">
        <h2 class="subheader">Settings</h2>
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
  name: "Blog",
  components: {
    Slider,
    SideBar,
  },
};
</script>