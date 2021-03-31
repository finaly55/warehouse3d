<template>
  <div class="home">
    <v-container>
      <v-card elevation="10" outlined id="bannercard">
        <v-btn
          @click="start"
          color=""
          elevation="2"
          outlined
          x-large
          id="btnstart"
          style="margin-top: 200px"
          >Commencez</v-btn
        >
      </v-card>
      <v-btn
        style="
          position: absolute;
          top: 5px;
          right: 5px;
          z-index: 300;
          display: none;
        "
        id="close-game"
        @click="close"
      >
        Fermer
      </v-btn>
    </v-container>
    <v-footer padless style="margin-top: 50px">
      <v-card flat tile class="indigo lighten-1 white--text text-center col-12">
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} | <strong>l'Usine Nantek</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  data() {
    return {
      dialog: false,
      icons: ["mdi-email", "mdi-instagram"],
    };
  },
  name: "Home",
  components: {
    HelloWorld,
  },
  methods: {
    start() {
      var container = document.querySelector("#unity-container");
      var closeGame = document.querySelector("#close-game");

      container.style.display = "block";
      document.documentElement.style.overflow = "hidden";
      closeGame.style.display = "block";
    },

    close() {
      var container = document.querySelector("#unity-container");
      var closeGame = document.querySelector("#close-game");

      container.style.display = "none";
      document.documentElement.style.overflow = "scroll";
      closeGame.style.display = "none";
    },
  },
};
</script>

<style>
#bannercard {
  margin-top: 100px;
  width: 100%;
  height: 500px;
}
#btnstart {
  margin: 15px;
  background-color: #ffee00;
}
</style>
