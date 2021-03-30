<template>
  <div id="app">
    <v-app-bar id="navbar">
      <img
        alt="Usine Nantek logo"
        src="./assets/usinenanteklogo.png"
        id="logo"
      />
      <div id="nav">
        <router-link to="/">Accueil</router-link> |
        <router-link to="/about">À propos</router-link>
      </div>
    </v-app-bar>

    <router-view />
  </div>
</template>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#navbar {
  background-color: #fff;
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
</style>
