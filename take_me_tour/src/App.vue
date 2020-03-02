<template>
  <v-app>
    <Navbar/>

    <v-content>
      <Home/>
    </v-content>
    <Footer/>
  </v-app>
</template>

<script>

import Navbar from './components/Navbar';
import Home from './views/Home';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Navbar,
    Home,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
