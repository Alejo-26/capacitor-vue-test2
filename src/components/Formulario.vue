<template>
  <div class="general">
    <div class="center">
      <section id="content">
        <h2 class="subheader">Registration</h2>
        <form class="mid-form" @submit.prevent="mostrarUsuario">
          <div class="form-group">
            <label for="nombre">Name</label>
            <input type="text" name="nombre" v-model="user.nombre" />
            <div v-if="!$v.user.nombre.required">This field is required</div>
          </div>

          <div class="form-group">
            <label for="apellidos">Last name</label>
            <input type="text" name="apellidos" v-model="user.apellidos" />
            <div v-if="submitted && !$v.user.apellidos.required">
              This field is required
            </div>
          </div>

          <div class="form-group">
            <label for="bio">Biografia</label>
            <textarea name="bio" v-model="user.bio"></textarea>
          </div>

          <div class="form-group radibuttons">
            <input
              type="radio"
              name="genero"
              value="hombre"
              v-model="user.genero"
            />
            Man
            <input
              type="radio"
              name="genero"
              value="mujer"
              v-model="user.genero"
            />
            Woman
            <input
              type="radio"
              name="genero"
              value="otro"
              v-model="user.genero"
            />
            Other
          </div>

          <div class="clearfix"></div>

          <input type="submit" value="Send" class="btn btn-success" />
        </form>

        <div class="datos" v-if="user.nombre && user.apellidos">
          <h3>{{ user.nombre + " " + user.apellidos }}</h3>
        </div>
      </section>

      <SideBar></SideBar>
      <div class="clearfix"></div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import { required, email, minLength } from "vuelidate/lib/validators";

import SideBar from "./SideBar.vue";

export default {
  name: "Formulario",
  components: {
    SideBar,
  },
  validations: {
    user: {
      nombre: {
        required,
        minLength: minLength(2),
      },
      apellidos: {
        required,
        minLength: minLength(2),
      },
    },
  },
  data() {
    return {
      submitted: false,
      user: {
        nombre: "",
        apellidos: "",
        bio: "",
        genero: "",
      },
    };
  },
  methods: {
    mostrarUsuario() {
      console.log(this.user);
      this.submitted = true;

      this.$v.$touch();
      if (this.$v.$invalid) {
        return false;
      }
      alert("Validacion pasada");
    },
  },
};
</script>