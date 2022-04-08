<template>
  <header id="header">
    <div class="center">
      <!-- LOGO -->
      <div id="logo">
        <img src="../assets/welcome-home.svg" class="app-logo" alt="Logotipo" />
        <span id="brand"> <strong>SHEMS</strong>  </span>
      </div>

      <!-- MENU -->
      <nav id="menu">
        <ul>
          <li>
            <router-link to="/home" active-class="active" @click.native="SaveIntoJsonFile('Home')">Home</router-link>
          </li>
          <li>
            <router-link to="/live-now" active-class="active">Live Now</router-link>
          </li>
          <li>
            <router-link to="/prosumer" active-class="active">Prosumer</router-link>
          </li>
          <li>
            <router-link to="/user" active-class="active">User</router-link>
          </li>
          <li>
            <!-- <router-link to="/mi-componente" active-class="active">Pagina 2</router-link> -->
            <router-link to="/settings" active-class="active">Settings</router-link>
          </li>
        </ul>
      </nav>

      <!--LIMPIAR FLOTADOS-->
      <div class="clearfix"></div>
    </div>
  </header>
</template>

<script>
/* eslint-disable */
export default {
  name: "HeaderComponent",
  methods: {
    //SaveDataintoaJsonfile
    SaveIntoJsonFile(command2){
      this.command = command2,
      this.date = Date.now()
      const fs = require('fs')
      fs.writeFile('./data45.json',JSON.stringify(this.data45,null,2), err=>{
        if (err){
          console.log(err)
        }
      });
    }
  },
  data(){
    return{
      data45:{
        command:'',
        date:''
      }
    }
  }
};
</script>

<style>
</style>