<template>
  <v-app>
    <Navbar/>

    <v-content>
      <router-view></router-view>
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
<style>
.TitelTxt{
    font-weight: 600!important;
    font-size: 26px;
    color: #4d4d5b;
    line-height: 9px;
    margin: 40px;
  }
  .v-btn{
    text-transform: capitalize!important;
  }
@media only screen and (min-width: 1264px) 
  and ( max-width: 2000px){
  .BodyBGcolot{
    background-color: #F8FBFB;
  }
  .childContainer{
    max-width: 1185px;
  }
}
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        body{
          overflow-x: hidden;
        }
        .TitelTxt{
          margin: 4px!important;
        }
        .BodyBGcolot{
          background-color: #F8FBFB;
        }
    }
</style>
