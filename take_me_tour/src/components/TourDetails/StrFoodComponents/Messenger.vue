<template>
  <v-container>
      <v-row class="hidden-sm-and-down">
          <p>Home <v-icon>mdi-chevron-right</v-icon> Bangkok <v-icon>mdi-chevron-right</v-icon> Street Food Tour in Bangkok Chinatown</p>
      </v-row>
      <v-row>
          <v-col md="8" lg="8" xl="8" cols="12">
              <h3 class="d-inline">Street Food Tour in Bangkok Chinatown</h3> 
          </v-col>
          <v-col cols="2"><v-btn class="ma-2 hidden-sm-and-down" text color="indigo"><v-icon>mdi-briefcase-upload-outline</v-icon> Share</v-btn></v-col>
          <v-col cols="2"><v-btn class="ma-2 hidden-sm-and-down" text color="indigo"><v-icon>mdi-heart-outline</v-icon> Wishlist</v-btn></v-col>
      </v-row>
      <v-row>
          <v-col cols="12" class="d-flex">
            <v-img class="mx-3" max-width="92" max-height="22" src="../../../assets/Tourimage/asset 11.png"></v-img> <span>Bangkok</span> 
          </v-col>

          <v-col cols="12" class="d-flex">
                <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating>
                <v-btn class="ma-2 hidden-sm-and-down white--text" color="indigo">50 reviews <v-icon>mdi-chevron-right</v-icon></v-btn>
          </v-col>
      </v-row>
      <v-row> <!--Massage section-->
          <v-col cols="9">
              <v-row>
                  <v-col cols="3">
                      <v-row>
                          <v-col cols="4"></v-col> <!--users-6-images-->
                      </v-row>
                  </v-col>
                  <v-col cols="9">
                      <p>Local Experience by</p>
                      <p>Selected Local Experts</p>
                  </v-col> <!--middel Text-->
              </v-row>
          </v-col>

          <v-col cols="3"></v-col><!--Massage Text & Icon-->
      </v-row>
      <v-row>
          <v-col cols="2">
            <v-icon></v-icon>
            <h5>Hosted by locals</h5>
            <p>3 Hours</p>    
          </v-col> <!--icons-->
      </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>

</style>