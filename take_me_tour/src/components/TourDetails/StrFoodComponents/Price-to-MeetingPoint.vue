<template>
  <v-container>
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
                  <v-col md="5" lg="5" xl="5" cols="12">
                      <h3>Meeting Points</h3>
                      <h5><v-icon>mdi-alpha-m-box</v-icon> MRT Stations</h5>
                      <p>- Hua Lamphong</p>
                      <p>- Wat Mangkon</p>
                  </v-col>
                  <v-col md="7" lg="7" xl="7" cols="12">
                      <v-card
                            class="mx-1 subheading "
                            elevation= 0
                            width="100%"
                            :ripple="false"
                        >
                            <v-img
                                class="white--text mapPic img align-end"
                                width="425"
                                height="342"
                                aspect-ratio="2"
                                src="../../../assets/Tourimage/asset 26.png"
                            >                    
                            </v-img>
                        </v-card>
                  </v-col>
              </v-row>
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>
.mapPic .v-image__image {
    background-size: inherit!important; 
}

</style>