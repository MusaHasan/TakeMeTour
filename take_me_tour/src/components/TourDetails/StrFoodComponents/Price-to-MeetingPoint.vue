<template>
  <v-containe>
      <v-row>
          <v-col cols="12">
              <h3>Price Conditions</h3>
              <p><v-icon>mdi-check</v-icon> Transportation fares are included. </p>
              <p><v-icon>mdi-check</v-icon> Admission fees are included </p>
              <p><v-icon>mdi-check</v-icon> Meals are included. </p>
          </v-col><!--Price Conditions-->
          <v-col cols="12">
              <h3>Why This Trip?</h3>
              <p>This particular tour is thoroughly screened and selected by the TakeMeTour team. 
                  Once you book this tour, we will assign it to our list of Local Experts with excellent 
                  know-how who are ready at your convenience to guide you through this trip.</p>
          </v-col><!--Why This Trip? How Local Is It? What Makes It Unique? < loop >-->
          <v-col cols="12">
              <v-row>
                  <v-col md="6" lg="6" xl="6" cols="12">
                      <h3>Meeting Points</h3>
                      <h5><v-icon>mdi-alpha-m-box</v-icon> MRT Stations</h5>
                      <p>- Hua Lamphong</p>
                      <p>- Wat Mangkon</p>
                  </v-col>
                  <v-col md="6" lg="6" xl="6" cols="12">
                      <v-card
                            class="ma-1 PopDesCrd"
                            height="216"
                            width="216"
                            :ripple="false"
                        >
                            <v-img
                                class="white--text img align-end"
                                height="100%"
                                src="../../../assets/Tourimage/asset 26.png"
                            >
                            <div class="fill-height pl-4 body-1">{{image.txt}}</div>                    
                            </v-img>
                        </v-card>
                  </v-col>
              </v-row>
          </v-col>
      </v-row>
  </v-containe>
</template>

<script>
export default {

}
</script>

<style>

</style>