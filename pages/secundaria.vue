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
<v-container>
      <h2 class="my-4 text-center text-h4">Aprendizaje Basado en Proyectos</h2>
      <v-row>
        <v-col cols="12">
          <v-card-actions class="justify-center">
            <div class="embed-responsive embed-responsive-16by9 justify-center">
              <iframe
                class="embed-responsive-item delimitador"
                :src="videoApren"
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
       <v-divider inset class="mt-5"></v-divider>
    </v-container>

      <div class="row">
        <div class="col-12 col-md-12 my-5" data-aos="fade-left">
          <h3 class="my-4 text-center text-h4">Materias</h3>
          <div class="row">
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/office/100/000000/ratings.png"
                />
              </p>
              <h4 class="text-center">Emprendimiento</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img src="https://img.icons8.com/office/100/000000/math.png" />
              </p>
              <h4 class="text-center">Matemáticas</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img src="https://img.icons8.com/office/100/000000/news.png" />
              </p>
              <h4 class="text-center">Español</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img src="https://img.icons8.com/dusk/100/000000/laptop.png" />
              </p>
              <h4 class="text-center">Computación</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-6">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/doodle/100/000000/germany.png"
                />
              </p>
              <h4 class="text-center">Alemán</h4>
            </div>

            <div class="col-12 mb-5 mb-md-0 col-md-6">
              <p class="text-center">
                <img
                  src="https://img.icons8.com/office/100/000000/talk-female.png"
                />
              </p>
              <h4 class="text-center">Inglés</h4>
            </div>
          </div>
        </div>

        <div class="col-12 col-md-12 mb-5" data-aos="fade-up">
          <h3 class="text-center mb-5">Apps de trabajo</h3>
          <div class="row">
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img
                  src="img/secundaria/canvas.png"
                  height="100"
                />
              </p>
              <h4 class="text-center">CANVAS</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img
                  src="img/secundaria/aleks.png"
                  height="100"
                />
              </p>
              <h4 class="text-center">ALEKS</h4>
            </div>
            <div class="col-12 mb-5 mb-md-0 col-md-3">
              <p class="text-center">
                <img
                  src="img/secundaria/achieve3000.png"
                  height="100"
                />
              </p>
              <h4 class="text-center">Achive 3000</h4>
            </div>
            <div class="col-12 col-md-3">
              <p class="text-center">
                <img
                  src="img/secundaria/gsuite.png"
                  height="100"
                />
              </p>
              <h4 class="text-center">G suite by Google</h4>
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
    title: 'Secundaria / CEA',
    meta: [
      {
        hid: 'Secundaria',
        name: 'description',
        content: 'ceacordoba secundaria'
      }
    ],
  },
  data() {
    return {
      title: 'SECUNDARIA CEA',
      description: `En Secundaria CEACORDOBA estamos comprometidos con la educación de nuestros
                alumnos
                brindando atención personalizada. Contamos con idiomas de inglés y alemán; así como también las
                materias de emprendimiento y calculo mental. Se trabaja con plataformas de alto rendimiento con el fin de que el alumno aprenda a su ritmo.
                Contamos con instalaciones que fomentan e inspiran la creatividad 
                en los alumnos brindando una estancia para el aprendizaje formidable.`,
      video:
        'https://www.youtube.com/embed/qlcmBqTUzWg',
      videoApren:'https://www.youtube.com/embed/HZmVM0KJDoc',
      items: [
        {
          src: '/img/secundaria/1.jpg',
          name: 'secundaria',
        },
        {
          src: '/img/secundaria/2.jpg',
          name: 'secundaria',
        },
        {
          src: '/img/secundaria/3.jpg',
          name: 'Secundaria',
        },
      ],
      fotos: [
        {
          src: `/img/secundaria/1.jpg`,
        },
        {
          src: `/img/secundaria/2.jpg`,
        },
        {
          src: `/img/secundaria/3.jpg`,
        },
        {
          src: `/img/secundaria/4.jpg`,
        },
        {
          src: `/img/secundaria/5.jpg`,
        },
        {
          src: `/img/secundaria/6.jpg`,
        },
        {
          src: `/img/secundaria/7.jpg`,
        },
        {
          src: `/img/secundaria/8.jpg`,
        },
        {
          src: `/img/secundaria/9.jpg`,
        },
        {
          src: `/img/secundaria/10.jpg`,
        },
        {
          src: `/img/secundaria/11.jpg`,
        },
        {
          src: `/img/secundaria/12.jpg`,
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
