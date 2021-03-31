<template>
  <div id="app">
    <v-app-bar id="navbar">
      <router-link to="/">
        <img
          alt="Usine Nantek logo"
          src="./assets/usinenanteklogo1.png"
          id="logo"
        />
      </router-link>
      <div id="nav">
        <router-link to="/"
          ><v-btn outlined class="btnnav">Accueil</v-btn></router-link
        >
        &nbsp;
        <router-link to="/about"
          ><v-btn outlined class="btnnav">À propos</v-btn></router-link
        >
      </div>
    </v-app-bar>

    <router-view />
  </div>
</template>
<script>
export default {
  created() {
    
  },
}
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");

#app {
  font-family: "Montserrat", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#navbar {
  background-color: #ffee00;
}
#nav {
  padding: 10px;
  margin: auto;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #4279b9;
}

#logo {
  width: 50px;
  height: 50px;
  margin-top: 5px;
  margin-left: 25px;
}
.btnnav:hover {
  background-color: #ffee00;
}
</style>
