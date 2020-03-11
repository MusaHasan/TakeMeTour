<template>
  <v-container>
      <v-row class="mx-md-0 mx-lg-0 mx-xl-0 mx-2">
          <h3 class="mb-3">Itinerary</h3>
          <v-col cols="12" class="orengeLine1"><span class="location"><v-icon color="orange darken-3">mdi-map-marker</v-icon></span></v-col>
          <v-col cols="12" class="py-0 textOrng"><span class="dot">.</span>18:30</v-col>
          <v-col cols="12" class="orengeLine2 py-2"> <p class="lightTxtP"> Meet up at MRT Station (Hua Lamphong, Wat Mangkon) </p></v-col>
          <v-col cols="12" class="py-0 textOrng"><span class="dot">.</span>  19:00</v-col>
          <v-col cols="12" class="orengeLine3 py-2" ><p class="lightTxtP">We'll start the trip by taking you to the numerous food stalls and restaurants hidden in the backstreets of <span style="color:#1cb6e6">Bangkok</span> Chinatown. Here! Let's taste some amazing Thai-Chinese food and desserts such as noodle, seafood, rice with barbecued pork, roasted duck, custard bun and cold Thai desserts. These are just a few examples!</p></v-col>
          <v-col cols="12" class="py-0 textOrng"><span class="dot">.</span>19:00</v-col>
          
          <v-col cols="12"><p class="lightTxtP">We'll start the trip by taking you to the numerous food stalls and restaurants hidden in the backstreets of <span style="color:#1cb6e6">Bangkok</span> Chinatown. Here! Let's taste some amazing Thai-Chinese food and desserts such as noodle, seafood, rice with barbecued pork, roasted duck, custard bun and cold Thai desserts. These are just a few examples!</p></v-col>
          <v-col cols="12"><p class="lightTxtP">When we finish drinking, I will send you back to MRT Wat Mangkon Station. Hope you enjoyed the trip, and have a good night!</p></v-col>

      </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>
  .lightTxtP{
    font-weight: 300 !important;
    line-height: 1.57 !important;
    font-size: 15px !important;
  }
  .orengeLine1,.orengeLine2,.orengeLine3{
    border-left: 2px solid #e86a1a;
    position: relative;
    top: 6px;
  }
  .orengeLine1{
    margin: 3px 0;
    height: 4px;
  }
  .orengeLine2{
    margin: -12px 0px 2px;
  }
  .orengeLine3{
    margin:-12px 0 3px;
  }
  .textOrng{
    color:#e86a1a;
  }
  .dot{
    color:#e86a1a;
    font-size: 5rem;
    position: absolute;
    margin: -73px -19px;
  }
  .location{
    font-size: 5rem;
    position: absolute;
    margin: -83px -25px;
  }
</style>