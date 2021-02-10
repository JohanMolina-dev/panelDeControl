<template>
  <div>
    <div v-if="estado">
      <div>
        <nav
          class="navbar navbar-expand-lg navbar navbar-dark bg-dark fixed-top"
        >
          <button
            class="navbar-toggler"
            type="button"
            data-toggle="collapse"
            data-target="#navbarTogglerDemo01"
            aria-controls="navbarTogglerDemo01"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          
        

          <div class="collapse navbar-collapse" id="navbarNav">
          
              
             
               <v-container>
                 <v-layout align-center justify-end row fill-height/>
                 <dir>
                    <v-btn
                  right
                  color="#FAC434"
                  v-on:click="ingresar"
                  :to="{ name: 'login' }"
                  elevation="10"
                >
                  Login</v-btn
                >
                 </dir>
                
              
               
               </v-container>
                 
          </div>
        </nav>
      </div>
      <hr>
      <carrousel-top></carrousel-top>
      <the-company></the-company>
   
      <div>
        <home />
      </div>
<footer-bar></footer-bar>
    </div>
    <div v-else>
      <v-app id="app">
        <v-navigation-drawer
          v-model="drawer"
          :clipped="$vuetify.breakpoint.lgAndUp"
          app
        >
          <v-list dense>
            <template>
              <v-list-item @click="home">
                <v-list-item-action>
                  <v-icon>home</v-icon>
                </v-list-item-action>
                <v-list-item-title> Inicio </v-list-item-title>
              </v-list-item>
            </template>
            <template v-if="logueado">
              <v-list-group>
                <v-list-item slot="activator">
                  <v-list-item-content>
                    <v-list-item-title> Almacén </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item :to="{ name: 'categoria' }">
                  <v-list-item-action>
                    <v-icon>table_chart</v-icon>
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title> Categorías </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item :to="{ name: 'articulo' }">
                  <v-list-item-action>
                    <v-icon>table_chart</v-icon>
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title> Artículos </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                 <v-list-item :to="{ name: 'tena' }">
                  <v-list-item-action>
                    <v-icon>table_chart</v-icon>
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title> Tena </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                 <v-list-item :to="{ name: 'bogota' }">
                  <v-list-item-action>
                    <v-icon>table_chart</v-icon>
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title> Bogotá </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-group>
              <v-list-group>
                <v-list-item slot="activator">
                  <v-list-item-content>
                    <v-list-item-title> Accesos </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item :to="{ name: 'usuario' }">
                  <v-list-item-action>
                    <v-icon>table_chart</v-icon>
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title> Usuarios </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-group>
            </template>
          </v-list>
        </v-navigation-drawer>
        <v-system-bar app color="#42A5F5">
          <v-spacer></v-spacer>
        </v-system-bar>
        <v-app-bar
          :clipped-left="$vuetify.breakpoint.lgAndUp"
          app
          color="#1976D2"
          dark
        >
          <v-toolbar-title style="width: 300px" class="ml-0 pl-3">
            <v-app-bar-nav-icon
              @click.stop="drawer = !drawer"
            ></v-app-bar-nav-icon>
            <span class="hidden-sm-and-down">Sistema</span>
          </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn @click="salir()" icon v-if="logueado">
            <v-icon>logout</v-icon> Salir
          </v-btn>
          <v-btn @click="salir()" icon v-else>
            <v-icon>logout</v-icon> Salir
          </v-btn>
        </v-app-bar>
        <v-content>
          <v-container fluid fill-height>
            <v-slide-y-transition mode="out-in">
              <router-view />
            </v-slide-y-transition>
          </v-container>
        </v-content>
     
      </v-app>
    </div>
  </div>
</template>

<script>
import CarrouselTop from "./components/CarrouselTop.vue";
import FooterBar from './components/FooterBar.vue';
import TheCompany from './components/TheCompany.vue';


import home from "./components/home.vue";
export default {
  components: { home, CarrouselTop, FooterBar, TheCompany },
  name: "App",

  data() {
    return {
      drawer: false,
      estado: 1,
    };
  },

  computed: {
    logueado() {
      return this.$store.state.usuario;
    },
  },
  created() {
    this.$store.dispatch("autoLogin");
  },
  methods: {
    salir() {
      this.$store.dispatch("salir");
      this.estado = 1;
    },

    ingresar() {
      this.estado = 0;
    },

    home() {
      this.estado = 1;
    },
  },
};
</script>
