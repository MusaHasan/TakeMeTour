<template>
  <v-container class="py-0">
      <v-row>
          <v-col cols="12">
              <h3 class="mb-4">Price Conditions</h3>
              <p class="mb-0"><v-icon color="rgb(239, 108, 0)">mdi-check</v-icon> Transportation fares are included. </p>
              <p class="mb-0"><v-icon color="rgb(239, 108, 0)">mdi-check</v-icon> Admission fees are included </p>
              <p class="mb-0"><v-icon color="rgb(239, 108, 0)">mdi-check</v-icon> Meals are included. </p>

            <div class="mt-6" style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->

          </v-col><!--Price Conditions-->
          <v-col cols="12" class="pb-0">
              <h3 class="mb-4">Why This Trip?</h3>
              <p class="mb-0">This particular tour is thoroughly screened and selected by the TakeMeTour team. 
                  Once you book this tour, we will assign it to our list of Local Experts with excellent 
                  know-how who are ready at your convenience to guide you through this trip.</p>
          </v-col><!--Why This Trip? How Local Is It? What Makes It Unique? < loop >-->
          <v-col class="pb-0" cols="12">
              <v-row>
                  <v-col class="py-0" md="5" lg="5" xl="5" cols="12">
                      <h3 class="mb-4">Meeting Points</h3>
                      <h5><v-icon>mdi-alpha-m-box</v-icon> MRT Stations</h5>
                      <p class="mb-0">- Hua Lamphong</p>
                      <p class="mb-0">- Wat Mangkon</p>
                  </v-col>
                  <v-col md="7" class="pa-0 " lg="7" xl="7" cols="12">
                      <v-card
                            class="subheading "
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

              <div class="mt-4" style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->

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
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .mapPic .v-image__image {
            background-size: contain!important;
            color: rgb(239, 108, 0);
        }

    .mapPic{
        height: 292px!important;
    }


    }
</style>