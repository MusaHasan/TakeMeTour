<template>
  <v-app>
    <Navbar/>

    <v-content>
      <HelloWorld/>
      <Home/>
    </v-content>
  </v-app>
</template>

<script>

import Navbar from './components/Navbar';
import HelloWorld from './components/HelloWorld';
import Home from './views/Home';

export default {
  name: 'App',

  components: {
    HelloWorld,
    Navbar,
    Home
  },

  data: () => ({
    //
  }),
};
</script>
