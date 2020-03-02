<template>
  <v-app>
    <Navbar/>

    <v-content>
      <!-- <HelloWorld/> -->
      <Home/>
    </v-content>
    <Footer/>
  </v-app>
</template>

<script>

import Navbar from './components/Navbar';
// import HelloWorld from './components/HelloWorld';
import Home from './views/Home';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    // HelloWorld,
    Navbar,
    Home,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
