<template>
  <v-container fluid class="pa-0">
    <video-bg class="mt-12 bg-dark" fluid :sources="['https://d34z6m0qj7i7g9.cloudfront.net/v5-assets/static/video/banner-short.mp4']" img="https://d34z6m0qj7i7g9.cloudfront.net/v5-assets/static/images/home/banner-video-placeholder.jpg">
    <!-- <video-bg :sources="['../assets/BGvideo/banner-short.mp4']" img="someURL"> -->
      <v-container class="bgGrayTanspherent white--text" max-he style="background-color: #00000082;" fluid>
        <v-row class="row-sm text-center">
          <v-col class="col-sm">
              <h2 class="headTitl-1 font-weight-medium">Explore Thailand & Southeast Asia with</h2>
              <h1 class="headTitl-2 ">Local Experts</h1>
            
            <v-img class="d-inline-block HeaderBodyImg pa-4" max-height="130" max-width="130"  src="../assets/images/asset 4.png"></v-img>
            <v-img class="d-inline-block HeaderBodyImg pa-4" max-height="130" max-width="130" src="../assets/images/asset 5.png"></v-img>
          </v-col>
        </v-row>
      </v-container>
    </video-bg>
    <search/>
  </v-container>
</template>

<script>
import search from './Search'
  export default {
    name: 'HelloWorld',

    components:{
      search,
    },
    data: () => ({
      ecosystem: [
        {
          text: 'vuetify-loader',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
        },
        {
          text: 'github',
          href: 'https://github.com/vuetifyjs/vuetify',
        },
        {
          text: 'awesome-vuetify',
          href: 'https://github.com/vuetifyjs/awesome-vuetify',
        },
      ],
      importantLinks: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com',
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com',
        },
        {
          text: 'Made with Vuetify',
          href: 'https://madewithvuejs.com/vuetify',
        },
        {
          text: 'Twitter',
          href: 'https://twitter.com/vuetifyjs',
        },
        {
          text: 'Articles',
          href: 'https://medium.com/vuetify',
        },
      ],
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/layout/pre-defined',
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>
<style>
.headTitl-1{
 font-size: 35px;
 font-family: Montserrat;
}
.headTitl-2{
font-size: 75px;
font-family: Montserrat;
}
.bgGrayTanspherent{
  height: 100%;
}
.row-sm, .col-sm{
  margin: 48px 0;
  padding: 48px 0;
}
@media only screen
and (min-device-width : 320px)
and (max-device-width : 767px) {
.VideoBg{
  height: 234px!important;
  }
.row-sm, .col-sm{
  margin: 0!important;
  padding: 0 !important;
}
.headTitl-2{
  font-size: 30px !important;
  font-weight: 300;
  line-height: 1rem;
}
.headTitl-1{
  font-size: 14px !important;
  font-weight: 400;
  line-height: 3.125rem;
}
.HeaderBodyImg{
  height: 75px;
  width: 75px;
}
}
@media only screen
and (min-device-width : 768px)
and (max-device-width : 1224px) {
  .VideoBg{
    height: 424px!important;
  }
  .row-sm, .col-sm{
    margin: 20px!important;
    padding: 0 !important;
  }
}
  
</style>
