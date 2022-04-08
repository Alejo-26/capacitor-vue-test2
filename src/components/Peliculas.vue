<template>
  <div class="general">
    <div class="center">
      <section id="content">
        <h2 class="subheader">Schedulling</h2>

        <div class="favorita" v-if="favorita2">
          La pelicula marcada es:
          <h3>{{favorita2.title}}</h3>
        </div>

        <!--Listado articulos-->
        <div id="articles">
          <!-- v-for="pelicula in peliculas" v-bind:key="pelicula.title" -->
          <div v-for="pelicula2 in peliculas" v-bind:key="pelicula2.title">
            <PeliculaComponent 
              :pelicula="pelicula2"
              @favorita="haLlegadoLaPeliculaFavorita"
            ></PeliculaComponent>
          </div>
        </div>
      </section>

      <SideBar></SideBar>
      <div class="clearfix"></div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import PeliculaComponent from "./PeliculaComponent.vue";
import SideBar from './SideBar.vue'
export default {
  name: "Peliculas",
  components: {
    PeliculaComponent,
    SideBar
  },
  methods:{
    haLlegadoLaPeliculaFavorita(favorita){
      console.log(favorita)
      alert('Se ha ejecutado el evento en el padre')
      this.favorita2=favorita

    }
  },
  data() {
    return {
      favorita2:null,
      peliculas: [
        {
          title: "Washing Machine",
          year: "Turn on at 8pm",
          image:
            "https://img.myloview.it/quadri/home-washing-machine-icon-outline-home-washing-machine-vector-icon-for-web-design-isolated-on-white-background-700-223977609.jpg",
        },
        {
          title: "Air Conditioner",
          year: "Turn off at 10pm",
          image:
            "https://www.svgrepo.com/show/89355/air-conditioner.svg",
        },
        {
          title: "Electric Vehicle",
          year: "Turn off at 5am",
          image:
            "https://pngimg.com/uploads/electric_car/electric_car_PNG17.png",
        }
      ],
    };
  },
};
</script>

<style>
</style>