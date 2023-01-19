<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="12" sm="6">
          <h1 class="lcea text-center mt-6">{{ title }}</h1>
          <v-row class="fill-height mt-4">
            <p class="text-justify subtitle-1">&nbsp; {{ description }}</p>
          </v-row>
        </v-col>
        <v-col class="text-center mt-5" cols="12" sm="6">
          <v-carousel
            cycle
            height="100%"
            hide-delimiter-background
            show-arrows-on-hover
            class="pa mb-16"
          >
            <v-carousel-item
              v-for="(item, i) in items"
              :key="i"
              :src="item.src"
              :lazy-src="item.src"
            >
            </v-carousel-item>
          </v-carousel>
        </v-col>
        <v-divider inset class="mt-5"></v-divider>
      </v-row>

      <div class="row">
        <div class="col-12 col-md-12 my-5" data-aos="fade-left">
          <h3 class="my-4 text-center text-h4">Materias Complementarias</h3>
          <div class="row">
            <div class="col-12 mb-5 mb-md-0 col-md-4">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/office/100/000000/talk-female.png"
                />
              </p>
              <h4 class="text-center">Inglés</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-4">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/dusk/100/000000/musical-notes.png"
                />
              </p>
              <h4 class="text-center">Ritmos y rondas</h4>
            </div>
            <div class="col-12 col-md-4">
              <p class="text-center">
                <img src="https://img.icons8.com/dusk/100/000000/laptop.png" />
              </p>
              <h4 class="text-center">Computación</h4>
            </div>
          </div>
        </div>

        <div class="col-12 col-md-12 mb-5" data-aos="fade-up">
          <h3 class="text-center mb-5">Talleres</h3>
          <div class="row">
            <div class="col-12 mb-5 mb-md-0 col-md-4">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/office/100/000000/taekwondo.png"
                />
              </p>
              <h4 class="text-center">Tae Kwando</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-4">
              <p class="text-center">
                <img src="https://img.icons8.com/dusk/100/000000/dancing.png" />
              </p>
              <h4 class="text-center">Baile Moderno</h4>
            </div>
            <div class="col-12 col-md-4">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/bubbles/100/000000/ping-pong.png"
                />
              </p>
              <h4 class="text-center">Tenis de Mesa</h4>
            </div>
          </div>
          <v-divider inset class="mt-5"></v-divider>
        </div>
      </div>
    </v-container>
    <h2 class="my-4 text-center text-h4">Galería</h2>
    <v-row>
      <v-col cols="12" sm="6" offset-sm="3">
        <v-card>
          <v-container fluid>
            <v-row>
              <v-col
                v-for="(foto, n) in fotos"
                :key="n"
                class="d-flex child-flex"
                cols="3"
              >
                <v-card flat tile class="d-flex">
                  <v-img
                    :src="foto.src"
                    :lazy-src="foto.src"
                    aspect-ratio="1"
                    class="grey lighten-2 img"
                  >
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
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
        <v-divider inset class="mt-5"></v-divider>
      </v-col>
    </v-row>

    <v-container>
      <h2 class="my-4 text-center text-h4">Vídeo</h2>
      <v-row>
        <v-col cols="12">
          <v-card-actions class="justify-center">
            <div class="embed-responsive embed-responsive-16by9 justify-center">
              <iframe
                class="embed-responsive-item delimitador"
                :src="video"
                min-width="900"
                min-height="500"
                style="border: none; overflow: hidden"
                scrolling="no"
                frameborder="0"
                allowfullscreen="true"
                allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
              ></iframe>
            </div>
          </v-card-actions>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Preescolar / CEA',
    meta: [
      {
        hid: 'Preescolar',
        name: 'description',
        content: 'ceacordoba preescolar o kinder'
      }
    ],
  },
  data() {
    return {
      title: 'PREESCOLAR CEA',
      description: `En el preescolar CEACORDOBA (Centro Educativo América) nos \
              distinguimos por respetar los tiempos de aprendizaje de cada\
              alumno acorde a su grado escolar también de madurez física, social\
              y emocional. Estimulamos el desarrollo de su creatividad e\
              imaginación a través de las artes visuales y música; realizan\
              exposiciónes sencillas de lo aprendido. En los alumnos se promueve\
              un ambiente de seguridad y respeto al relacionarse y comunicarse.`,
      video:
        'https://drive.google.com/file/d/1S2I2PxhKvWcgEg4kdIVGETO9VT5zUNyN/preview',
      items: [
        {
          src: '/img/preescolar/10.jpg',
          name: 'Preescolar',
        },
        {
          src: '/img/preescolar/12.jpg',
          name: 'Primaria',
        },
        {
          src: '/img/preescolar/14.jpg',
          name: 'Secundaria',
        },
      ],
      fotos: [
        {
          src: `/img/preescolar/01.jpg`,
        },
        {
          src: `/img/preescolar/02.jpg`,
        },
        {
          src: `/img/preescolar/03.jpg`,
        },
        {
          src: `/img/preescolar/04.jpg`,
        },
        {
          src: `/img/preescolar/05.jpg`,
        },
        {
          src: `/img/preescolar/06.jpg`,
        },
        {
          src: `/img/preescolar/07.jpg`,
        },
        {
          src: `/img/preescolar/08.jpg`,
        },
        {
          src: `/img/preescolar/14.jpg`,
        },
        {
          src: `/img/preescolar/10.jpg`,
        },
        {
          src: `/img/preescolar/13.jpg`,
        },
        {
          src: `/img/preescolar/12.jpg`,
        },
      ],
    }
  },
}
</script>

<style>
.img:hover {
  -webkit-transform: scale(1.3);
  transform: scale(1.3);
  transition: 0.2s;
  z-index: 1000;
}


@media (min-width: 700px) {
  .delimitador {
    width: 65vw; /* Ancho máximo */
    height: 50vh;
    margin: auto;
  }
}
iframe {
  height: 100%;
  width: 100%;
  top: 0px;
  left: 0px;
}
</style>
