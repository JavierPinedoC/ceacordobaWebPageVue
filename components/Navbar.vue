<template>
 <div>
     <v-app-bar app class="blue darken-4  text-center" >
      <v-toolbar-title>
        <NuxtLink to="/" tag="span" style="cursor: pointer">
          <span class="lceab white--text">
            {{ appTitle }}
          </span>
          <span class="letracolor" v-if="$nuxt.$route.name == 'preescolar'"> {{menuItems[1].namePa}} </span>
          <span class="letracolor" v-else-if="$nuxt.$route.name == 'primaria'"> {{menuItems[2].namePa}} </span>
          <span class="letracolor" v-else-if="$nuxt.$route.name == 'secundaria'"> {{menuItems[3].namePa}} </span>
           <span class="letracolor" v-else> {{menuItems[0].namePa}} </span>
        </NuxtLink>
      </v-toolbar-title>
      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-xs-only ">
        <v-btn text v-for="item in menuItems" :key="item.title" :to="item.path" class="white--text text-center">
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-app-bar-nav-icon
        @click="drawer = true"
        class="d-flex d-sm-none"
      ></v-app-bar-nav-icon>
    </v-app-bar>
    
    <v-navigation-drawer v-model="drawer"  temporary bottom app >
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-blue--text text--accent-4"
        >
          <v-list-item
            v-for="item in menuItems"
            :key="item.title"
            :to="item.path"
          >
            <v-list-item-title> {{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
 </div>
</template>

<script>
export default {
  data() {
    return {
       
      appTitle: `CEACORDOBA`,
      sidebar: false,
      menuItems: [
        { title: 'Inicio', path: '/', namePa:'| EDUCACIÓN BÁSICA' },
        { title: 'Preescolar', path: '/preescolar', namePa:'| PREESCOLAR' },
        { title: 'Primaria', path: '/primaria', namePa:'| PRIMARIA' },
        { title: 'Secundaria', path: '/secundaria', namePa:'| SECUNDARIA' },
      ],
      drawer: false,
      group: null,
    }
  },
}
</script>

<style>
.letracolor{
  color: #7dcada;
}
v-navigation-drawer{
  position: relative;
height: calc(100vh );
overflow: auto;
}
</style>
