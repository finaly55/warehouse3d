<template>
    <div class="home" style="background-color: #ffec0c;">
    <v-container>
      <v-card
        elevation="10"
        outlined
        id="bannercard"
        style="background-color: #ffec0c; border: none;"
      >
        <v-container>
          <v-row class="mb-6" no-gutters>
            <v-col sm="5" md="5">
              <img
                alt="Usine Nantek logo"
                src="../assets/usinenanteklogo1.png"
                id="logo"
              />
            </v-col>
            <v-col sm="7" md="7">
              <p id="bannertext" style="">
                <strong>Vivez une nouvelle expérience !</strong>
              </p>
            </v-col>
          </v-row>
        </v-container>
        <v-btn elevation="2" x-large id="btnstart" @click="start"
          ><v-icon style="color: white"> mdi-rocket </v-icon> &nbsp;
          <span id="textbtnstart"><strong>Lancer</strong></span>
        </v-btn>
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
    <v-footer padless style="margin-top: 50px; background-color: #ffec0c">
      <v-card
        flat
        tile
        class="text-center col-12"
        style="background-color: #ffec0c"
      >
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            class="mx-4 white--text"
            :href="icon.url"
            icon
          >
            <v-icon size="24px">
              {{ icon.icon }}
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
      icons: [
        { url: "mailto:lusine.nantek@gmail.com", icon: "mdi-email" },
        {
          url: "https://www.instagram.com/lusine_nantek/",
          icon: "mdi-instagram",
        },
      ],
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
      container.style.top = "0";
      container.style.left = "0";
      document.documentElement.style.overflow = "hidden";
      closeGame.style.display = "block";

      var loaderUrl = buildUrl + "/neoclub-unity-poc-build.loader.js";

      var script = document.createElement("script");
      script.src = loaderUrl;
      script.onload = () => {
        createUnityInstance(canvas, config, (progress) => {
          progressBarFull.style.width = 100 * progress + "%";
        })
          .then((unityInstance) => {
            loadingBar.style.display = "none";
          })
          .catch((message) => {
            alert(message);
          });
      };
      document.body.appendChild(script);
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
  background-color: #3555a2;
  margin-left: 300px;
}
#btnstart:hover {
  background-color: #2177c7;
}
#textbtnstart{
  color: white;
  font-size: 22px;
  margin-left: 10px;
}
#logo {
  width: 250px;
  height: 250px;
  float: right;
  margin-right: 100px;
}
#bannertext {
  font-size: 48px;
  margin-top: 100px;
  color: #3555a2;
  float: left;
}
</style>
© 2021 GitHub, Inc.