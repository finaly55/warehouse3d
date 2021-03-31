<template>
  <div id="app">
    <v-app-bar id="navbar">
      <div id="nav">
        <router-link to="/" class="navbtn">Accueil</router-link> | &nbsp;
        <router-link to="/about" class="navbtn">À propos</router-link>
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
  color: #3555a2;
}
#navbar {
  background-color: #ffec0c;
}
#nav {
  padding: 10px;
  margin: auto;
}

#nav a {
  font-weight: bold;
  color: #3555a2;
}

#nav a.router-link-exact-active {
  color: #3555a2;
}

#logo {
  width: 50px;
  height: 50px;
  margin-top: 5px;
  margin-left: 25px;
}

.navbtn {
  font-size: 18px;
}
</style>
