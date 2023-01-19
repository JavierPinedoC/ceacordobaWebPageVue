<template>
  <v-footer dark padless>
    <v-card
      flat
      tile
      width="100%"
      class="blue darken-4 white--text text-center"
    >
      <v-card-text class="mt-5">
        <v-btn
          v-for="icon in icons"
          :key="icon.id"
          :href="icon.url"
          target="_blank"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon.redname }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-container>
        <v-card elevation="13" outlined shaped class="blue-grey darken-1">
          <v-card-title> </v-card-title>

          <v-row justify="center" v-for="item in info" :key="item.id">
            <v-col cols="12" sm="6">
              <h1 class="display-1 mb-5">Contacto - {{ item.escuela }}</h1>
              <p class="card-text">
                Estamos situados en
                <strong>{{ item.direccion }}</strong> <br />
                En horario de {{ item.horario.horas }} hrs. de
                {{ item.horario.dias }} <br />
                Marcanos al <strong>{{ item.tel }}</strong> <br />
                Escribenos al
                <strong>{{ item.email }}</strong>
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <p class="card-text">
                <iframe
                  :src="item.map"
                  max-height="300"
                  max-width="600"
                  frameborder="0"
                  style="border: 0"
                  allowfullscreen=""
                  aria-hidden="false"
                  tabindex="0"
                ></iframe>
              </p>
            </v-col>
          </v-row>

          <v-divider></v-divider>

          <v-card-subtitle class="white--text">
            <strong>Tu mejor opción de enducación</strong>
          </v-card-subtitle>
        </v-card>
      </v-container>
      <v-divider></v-divider>

      <v-card-text class="white--text lceab">
        {{ new Date().getFullYear() }} - <strong class="">CEACORDOBA</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      { redname: 'mdi-facebook', url: 'https://www.facebook.com/CEACOR' },
      { redname: 'mdi-twitter', url: 'https://wwww.twitter.com/CEACordoba' },
      {
        redname: 'mdi-instagram',
        url: 'https://www.instagram.com/ceacordoba/',
      },
    ],
    info: [
      {
        escuela: 'Preescolar y Primaria',
        direccion: 'Calle 11, #514, centro en Córdoba, Ver.',
        horario: { horas: '10:00 a 14:00', dias: 'Lunes a Viernes' },
        tel: '271-714-6149',
        email: 'centroeducativoamerica@hotmail.com',
        map:
          'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3774.9281369082087!2d-96.9351406847571!3d18.890268987194812!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85c4e5428d3563ed%3A0x64461c555170cfe3!2sCentro%20Educativo%20America%20%2F%20CEACORDOBA!5e0!3m2!1ses-419!2smx!4v1596583233229!5m2!1ses-419!2smx',
      },
      {
        escuela: 'Secundaria',
        direccion: 'Av. 15, #307, Alameda, Córdoba, Ver.',
        horario: { horas: '10:00 a 14:00', dias: 'Lunes a Viernes' },
        tel: '271-714-6149',
        email: 'centroeducativoamerica@hotmail.com',
        map:
          'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d396.79426180841904!2d-96.93833010836242!3d18.88865712899244!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85c4e5417143fcb5%3A0xe709485449e4ae9d!2sAv%2015%20307%2C%20Alameda%2C%2094580%20C%C3%B3rdoba%2C%20Ver.!5e0!3m2!1ses-419!2smx!4v1612582004596!5m2!1ses-419!2smx',
      },
    ],
  }),
}
</script>

<style></style>
