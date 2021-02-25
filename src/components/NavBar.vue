<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      app
      color="#43a047"
      dark
      shrink-on-scroll
      prominent
      src="https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-2"
      scroll-threshold="500"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(55,236,186,.7), rgba(25,32,72,.7)"
        />
      </template>
      <v-app-bar-nav-icon/>

      <v-app-bar-title>Title</v-app-bar-title>

      <v-spacer/>

<!--      <div class="d-flex align-center">-->
<!--        <v-img-->
<!--          alt="Vuetify Logo"-->
<!--          class="shrink mr-2"-->
<!--          contain-->
<!--          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"-->
<!--          transition="scale-transition"-->
<!--          width="40"-->
<!--        />-->

<!--        <v-img-->
<!--          alt="Vuetify Name"-->
<!--          class="shrink mt-1 hidden-sm-and-down"-->
<!--          contain-->
<!--          min-width="100"-->
<!--          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"-->
<!--          width="100"-->
<!--        />-->
<!--      </div>-->

<!--      <v-switch-->
<!--        v-model="$vuetify.theme.dark"-->
<!--        inset-->
<!--        label="Vuetify Theme Dark"-->
<!--        class="dark-switch"-->
<!--      />-->
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <router-link to="/" class="router-link-btn">
        <v-btn
          color="#fff"
          text
        >
          <span>
            Home
          </span>
        </v-btn>
      </router-link>
      <router-link to="/profile" class="router-link-btn">
        <v-btn
          color="#fff"
          text
        >
          Profile
        </v-btn>
      </router-link>
      <router-link to="/about" class="router-link-btn">
        <v-btn
          color="#fff"
          text
        >
          About
        </v-btn>
      </router-link>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"
      max-height="600"
    >
      <Home/>
<!--      <router-view/>-->
<!--      <v-container style="height: 1500px;"></v-container>-->
    </v-sheet>
  </v-card>
</template>

<script>
import Home from '../views/Home.vue';

export default {
  components: {
    Home,
  },
};
</script>

<style>
  #nav {
    padding: 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }
  .router-link-btn {
    text-decoration: none;
  }
  .dark-switch {
    margin-top: 8px !important;
  }
</style>
