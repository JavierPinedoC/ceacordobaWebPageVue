<template>
  <div>
    <!-- <v-parallax dark max-height="100%" src="/img/ceaalwaysontop.jpg">
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12" sm="6">
          <v-card elevation="16" shaped class="border">
            <h1 class="mb-4 lceab black--text">CEACORDOBA</h1>
            <h2 class="subheading black--text">Tu mejor opción en educación</h2>
          </v-card>
        </v-col>
      </v-row>
    </v-parallax> -->

    <v-carousel
      cycle
      height="810"
      hide-delimiter-background
      show-arrows-on-hover
      class="pa mb-16"
    >
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row class="fill-height" align="center" justify="center">
          <div class="display-3 text-center">
                  <div class="offer border2 rounded">
              {{ item.offer }}
            </div>
            {{ item.name }} <br /><br />
     
          </div>
        </v-row>
      </v-carousel-item>
    </v-carousel>

    <v-container>
      <v-row align="center mx-auto" justify="center">
        <v-col cols="12" sm="6">
          <h1 class="display-3 mb-5">Nosotros</h1>
          <p class="text-justify">
            &nbsp; Somos una escuela que cuenta con los niveles de jardín y
            primaria, por lo que en este ciclo que celebramos 20 años de dar
            excelente servicio educativo, vamos a abrir el nivel secundaria.
            <br /><br />
            &nbsp; Nos destacamos por la atención  personalizada que se les
            brinda a sus alumnos ya que nuestros grupos son pequeños con esto
            tener una mayor atención a las necesidades de los mismos,
            haciéndoles sentir en un ambiente familiar y brindarles siempre
            seguridad. Ofrecemos educación basada en competencias con enfoque en
            idiomas por lo que contamos con inglés y alemán así como con ajedrez
            y música, de igual forma los impulsamos a practicar diversas 
            actividades deportivas.
          </p>
        </v-col>
        <v-col cols="12" sm="3">
          <v-img
            lazy-src="/img/logoCEA.png"
            max-height="300"
            max-width="300"
            aspect-ratio="1"
            src="/img/logoCEA.png"
          ></v-img>
        </v-col>
      </v-row>

      <v-divider inset class="mt-5"></v-divider>
    </v-container>

    <div>
      <v-container>
        <v-row justify="center">
          <v-col>
            <h2 class="text-center">Calificación escolar (Planea)</h2>

            <p class="text-justify">
              Nos enorgullece el presentar una calificación que con mucho
              esfuerzo y dedicación de nuestros alumnos y docentes se ha
              logrado, hemos presentado la prueba de Planea y se logró una
              calificación excelente. El Centro Educativo América sigue
              esforzándose y manteniendo altos estándares de enseñanza para que
              el aprendizaje hacía nuestros alumnos desarrollen sus habilidades.
              <br />
              <a
                target="_blank"
                href="http://www.mejoratuescuela.org/escuelas/index/30PPR3647E"
              >
                Ver más</a
              >
            </p>
          </v-col>
          <v-col>
            <v-img
              lazy-src="/img/logoCEA.png"
              max-height="824"
              max-width="1415"
              contain
              class="img"
              src="/img/calif.png"
            ></v-img>
          </v-col>
        </v-row>
        <v-divider insert class="mt-5"></v-divider>
      </v-container>
    </div>

    <div>
      <v-container>
        <v-row class="text-center" justify="center">
          <v-col cols="12" sm="4" v-for="item in flyer" :key="item.name">
            <v-img
              class="white--text align-end img"
              height="760px"
              :src="item.src"
            >
              <!-- <v-card-title>Top 10 Australian beaches</v-card-title> -->
            </v-img>
          </v-col>
        </v-row>
        <v-divider inset class="mt-5"></v-divider>
      </v-container>
    </div>

    <div>
      <v-container>
        <h1 class="mb-4 lceab text-center my-5">CEACORDOBA</h1>
        <v-row align="center mx-auto" justify="center">
          <v-col cols="12" sm="4" v-for="item in imgP" :key="item.title">
            <v-card class="" max-width="400">
              <v-img
                class="white--text align-end"
                height="229px"
                :src="item.img"
                :lazy-src="item.img"
              >
                <!-- <v-card-title>Top 10 Australian beaches</v-card-title> -->
                <template v-slot:placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                  >
                    <v-progress-circular
                      indeterminate
                      color="grey lighten-5"
                    ></v-progress-circular>
                  </v-row>
                </template>
              </v-img>

              <v-card-subtitle class="pb-0">{{ item.title }}</v-card-subtitle>

              <v-card-text class="text--primary">
                <div>{{ item.texto }}</div>
              </v-card-text>

              <v-card-actions>
                <v-btn color="blue" :to="item.path" text>
                  Más información
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  data() {
    return {
      imgP: [
        {
          title: 'Preescolar',
          texto:
            'En el preescolar CEACORDOBA (Centro Educativo América) nos distinguimos por respetar los tiempos...',
          path: '/preescolar',
          img: '/img/Preescolar.jpg',
        },
        {
          title: 'Primaria',
          texto:
            'En primaria CEACORDOBA estamos comprometidos con la educación de nuestros alumnos brindando atención personalizada...',
          path: '/primaria',
          img: '/img/PrimariaCEA.jpg',
        },
        {
          title: 'Secundaria',
          texto:
            'En Secundaria CEACORDOBA estamos comprometidos con la educación, creatividad e innovación hacía nuestros alumnos brindando atención personalizada...',
          path: '/secundaria',
          img: '/img/Secundaria.jpg',
        },
      ],
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4',
      ],
      slides: [],
      items: [
        {
          src: '/img/Preescolar.jpg',
          name: 'Preescolar',
          offer: 'Estamos orgullosos de ser una escuela Bilingüe',
        },
        {
          src: '/img/PrimariaCEA.jpg',
          name: 'Primaria',
          offer: 'Estamos orgullosos de ser una escuela Bilingüe',
        },
        {
          src: '/img/Secundaria.jpg',
          name: 'Secundaria',
          offer: 'Estamos orgullosos de ser una escuela Bilingüe',
        },
      ],
      flyer: [
        {
          src: '/img/Flyer/preescolar22-23.jpeg',
          name: 'Preescolar',
        },
        {
          src: '/img/Flyer/primaria22-23.jpeg',
          name: 'Primaria',
        },
        {
          src: '/img/Flyer/secundaria22-23.jpeg',
          name: 'Secundaria',
        },
      ],
    }
  },
  components: {
    Logo,
    VuetifyLogo,
  },
}
</script>

<style>
.border {
  background-color: #ffffff;
  opacity: 0.6;
}
.pa {
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
}
.img:hover {
  -webkit-transform: scale(1.3);
  transform: scale(1.3);
  transition: 0.2s;
  z-index: 1000;
}
.offer{
  color: rgba(0, 0, 114, 0.842);
  font-weight: bolder;
}
.border2 {
  background-color: #00114f03;
 
}
</style>
