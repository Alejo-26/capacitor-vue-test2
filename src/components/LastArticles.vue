<template>
  <div class="general">
    <Slider
      texto="Welcome to SHEMS"
      texto2="Saving the planet and your wallet"
    ></Slider>
    <div class="center">
      <section id="content">
        <h2 class="subheader">Appliances turned on</h2>

        <!--Listado articulos-->
        <div id="articles">
          <article class="article-item" id="article-template">
            <div class="image-wrap">
              <img
                src="../assets/washing-machine.svg"
                alt="Paisaje"
              />
            </div>

            <h2>Washing Machine</h2>
            <span class="date"> LG F4WV310S6E </span>
            <a href="#">Turn it off</a>

            <div class="clearfix"></div>
          </article>

          <!--AÑADIR ARTICULOS VIA JS-->
        </div>
      </section>
      <SideBar></SideBar>
      <div class="clearfix"></div>
    </div>
  </div>
</template>

<script>
import Slider from "./Slider";
import SideBar from "./SideBar.vue";
export default {
  name: "LastArticles",
  components: {
    Slider,
    SideBar,
  },
};
</script>

<style>
</style>