<template>
  <div class="about">
    <v-container>
      <v-alert color="#2A3B4D" dark icon="mdi-pencil" dense class="col-4"
        ><h2>L'usine Nantek en quelques mots</h2>
      </v-alert>
      <v-alert color="#2A3B4D" dark outlined>
        <h3>
          <p>
            L'usine Nantek est une agence nantaise qui répond à vos demande de
            créations digitales.
          </p>
          <br />
          <p>
            Soucieux de vous satisfaire, nous mettons tout en œuvre pour trouver
            des solutions qui sauront satisfaire l'exigence de vos attentes.
          </p>
          <br />
          <p>
            Les domaines variés que représentent nos équipiers rendent l'usine
            Nantek unique et qualifiée. Motivation, créativité, respect et
            professionnalisme sont les mots d'ordre de notre agence.
          </p>
        </h3>
      </v-alert>
    </v-container>
    <v-container>
      <div>
        <v-alert
          color="#2A3B4D"
          dark
          icon="mdi-firework"
          dense
          class="col-4"
          id="aboutcard"
        >
          Découvrez l'équipe de L'usine Nantek' !
        </v-alert>
      </div>
      <v-card id="cardteam">
        <v-row>
          <v-col>
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/1.png" alt="John" />
                </v-col>
                <v-col class="desc-text">Team Manager | Développeur</v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col>
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/2.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Développeur </v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col>
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/3.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Développeur </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/4.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Artiste 3D </v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/5.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Artiste 3D </v-col>
              </v-row>
            </v-card></v-col
          >
          <v-col
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/6.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Artiste 3D </v-col>
              </v-row>
            </v-card></v-col
          >
        </v-row>
        <v-row>
          <v-col>
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/7.png" alt="John" />
                </v-col>
                <v-col class="desc-text">
                  Admnistrateur système et réseau
                </v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/8.png" alt="John" />
                </v-col>
                <v-col class="desc-text">
                  Admnistrateur système et réseau
                </v-col>
              </v-row>
            </v-card></v-col
          >
          <v-col
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/9.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Chargé évenementiel </v-col>
              </v-row>
            </v-card></v-col
          >
        </v-row>
        <v-row>
          <v-col>
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/10.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Chargé évenementiel </v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/11.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Chargé en communication </v-col>
              </v-row>
            </v-card></v-col
          >
          <v-col
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/12.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Développeur </v-col>
              </v-row>
            </v-card></v-col
          >
        </v-row>
        <v-row>
          <v-col class="col-4">
            <v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/13.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Développeur </v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col class="col-4"
            ><v-card id="uniqueavt">
              <v-row>
                <v-col>
                  <img src="../assets/13.png" alt="John" />
                </v-col>
                <v-col class="desc-text"> Développeur </v-col>
              </v-row>
            </v-card></v-col
          >
        </v-row>
      </v-card>
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
          {{ new Date().getFullYear() }} | <strong>l'Usine Nantek'</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: ["mdi-email", "mdi-instagram"],
    };
  },
};
</script>


<style>
#uniqueavt {
  margin: 10px;
  font-size: 1.2rem;
}
img {
  width: 100px;
  height: 100px;
  border-radius: 50px;
}
#aboutcard {
  margin-top: 100px;
}

#cardteam {
  margin-top: 25px;
  box-shadow: none;
  border: none;
}
.desc-text {
  margin-top: 40px;
}
</style>
