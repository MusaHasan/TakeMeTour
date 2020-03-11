<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container class="childContainer">
      <v-row >
          <h2 class="TitelTxt mb-6">Popular Destinations</h2>
        <v-sheet
          class="mx-auto transparent"
          elevation="0"
          max-width="100%"
        >
          <v-slide-group
            class="pa-0 sliderContainer"
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
              class="ml-2 transparent"
            >
              <v-card
                class="ma-1 PopDesCrd"
                height="216"
                width="216"
                :ripple="false"
              >
                <v-img
                    class="white--text img align-end"
                    height="100%"
                    :src="require(`../../assets/images/${image.name}`)"
                    gradient="to bottom, rgba(241, 241, 241, 0.01), rgba(0, 0, 0, 0.9)"
                >
                  <div class="fill-height mb-4 pl-4 body-1">{{image.txt}}</div>                    
                </v-img>
              </v-card>
              
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-row>
  </v-container>
</v-container>
</template>

<script>
export default {
     data:()=>({
        images:[
            {
                name:'asset 42.jpeg', txt:'Phuket'
            },
            {
                name:'asset 43.jpeg', txt:'Siem Reap'
            },
            {
                name:'asset 44.jpeg', txt:'Saigon'
            },
            {
                name:'asset 45.jpeg', txt:'Manila'
            },
            {
                name:'asset 46.jpeg', txt:'Bangkok'
            },
            {
                name:'asset 47.jpeg', txt:'Bali'
            },
            {
                name:'asset 48.jpeg', txt:'Chiang Mai'
            },
            {
                name:'asset 49.jpeg', txt:'Phnom Penh'
            }
        ]
    })
}
</script>

<style>
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
    .PopDesCrd{
      width: 125px!important;
      height: 125px!important;
    }
 }

</style>