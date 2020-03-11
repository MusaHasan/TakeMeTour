<template>
  <v-container>
    <h3 class="pb-3">Explore This Trip</h3>
      <v-row class="hidden-sm-and-down">
        
          <v-col class="px-0 Ex-images " cols="3" v-for="(image,i) in images"
              :key="i" >
              <v-card
                class="ma-1 PopDesCrd"
                style="border-redius:16px!important"
                height="225"
                width="180"
                :ripple="false" 
              >
                <v-img
                    class="white--text img align-end"
                    height="225"
                    width="180"
                    :src="require(`../../../assets/images/${image.name}`)"
                    gradient="to bottom , rgba(255, 250, 250, 0.01),rgba(255, 250, 250, 0.01), rgba(191, 195, 217, 0.2), rgba(191, 195, 217, 0.2), rgba(0, 0, 0, 0.99)"
                >
                  <div class="fill-height text-center bottom-gradient">{{image.txt}}</div>                    
                </v-img>
              </v-card>
              
          </v-col>
          
      </v-row >
      
      <div class="mt-4 hidden-sm-and-down" style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->

      <v-row class="hidden-md-and-up">
        <v-sheet
          class="mx-auto transparent"
          elevation="0"
          max-width="100%"
        >
          <v-slide-group
            class="pa-0"
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
              class="ml-2 transparent"
            >
              <v-card
                class="ma-1 ExplCrd"
                :ripple="false"
              >
                <v-img
                    class="white--text img align-end"
                    height="100%"
                    :src="require(`../../../assets/images/${image.name}`)"
                    gradient="to bottom , rgba(255, 250, 250, 0.01),rgba(255, 250, 250, 0.01), rgba(191, 195, 217, 0.2), rgba(191, 195, 217, 0.2), rgba(0, 0, 0, 0.99)"
                >
                  <div class="fill-height text-center pl-4 body-1">{{image.txt}}</div>                    
                </v-img>
              </v-card>
              
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-row>
      <div class="mt-4 hidden-md-and-up" style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->
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
  .Ex-images .v-card{
    border-radius: 15px!important;
  }
  .ExplCrd{
    height: 216px !important;
    width: 216px !important;
  }
    @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .ExplCrd{
        width: 240px!important;
        height: 300px!important;
        border-radius: 15px!important;
        }
    }
</style>