<template>
  <v-app>
    <Toolbar />
    <v-content id="main-container">
      <router-view />
    </v-content>
    <Footer />

  </v-app>
</template>

<script>
import Toolbar from './components/Toolbar';
import Footer from './components/Footer'



export default {
  name: 'App',

  components: {
    Toolbar,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
#main-container {
  background-color: white;
}
</style>