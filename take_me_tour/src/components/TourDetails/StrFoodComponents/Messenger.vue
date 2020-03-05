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
            <v-img class="mx-3" max-width="92" max-height="22" src="../../../assets/Tourimage/asset 11.png"></v-img> <span class="blueTxt">Bangkok</span> 
          </v-col>

          <v-col md="12" lg="12" xl="12" cols="6" class="d-flex">
                <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating>
                <v-btn class="ma-2 white--text" color="green darken-2">50 reviews <v-icon>mdi-chevron-right</v-icon></v-btn>
          </v-col>
      </v-row>
      <v-row class="bgLiteBlue"> <!--Massage section-->
          <v-col class="py-0" cols="12">
              <v-row>
                  <v-col class="px-md-12 px-lg-12 px-3 py-0" md="3" lg="3" xl="3" cols="2">
                      <v-row>
                          <v-col v-for="(user,i) in users" :key="i" class="py-0 px-0" cols="4">
                              <v-list-item-avatar min-width="18"
                              width="18" height="18"
                                 color="grey darken-3">
                                    <v-img
                                        class="elevation-6"
                                        src="../../../assets/Tourimage/asset 14.png"
                                    ></v-img>
                                </v-list-item-avatar>
                          </v-col> <!--users-6-images-->
                      </v-row>
                  </v-col>
                  <v-col class="py-0 pr-0 mt-2" cols="7">
                      <p class="my-0">Local Experience by</p>
                      <p style="color:#16c464!important;">Selected Local Experts</p>
                  </v-col> <!--middel Text-->
                  
                  <v-col class="py-0 px-0" md="2" lg="2" xl="2" cols="2">
                    <p class="blueTxt my-5"><v-icon color="rgb(28, 182, 230)">mdi-comment-text-multiple-outline</v-icon> Massage</p>
                  </v-col><!--Massage Text & Icon-->
              </v-row>
          </v-col>

      </v-row>
      <v-row >

        <v-col class="mx-md-10 mx-lg-10 mx-xl-10 px-6" md="2" lg="2" xl="2" cols="4">
            <v-avatar color="white" size="62">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 90.jpg"
                    ></v-img>
            </span>
            </v-avatar>
            <h5>Hosted by locals</h5>
            <p>3 Hours</p>    
        </v-col> <!--icons-->

        <v-col class="px-6" md="2" lg="2" xl="2" cols="4">
            <v-avatar color="white" size="62">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 91.jpg"
                    ></v-img>
            </span>
            </v-avatar>
            <h5>Hosted by</h5>
            <p>3 Hours</p>    
        </v-col> <!--icons-->

        <v-col class="px-6" md="2" lg="2" xl="2" cols="4">
            <v-avatar color="white" size="62">
                <span class="white--text headline">
                    <v-img
                            class="elevation-0"
                            src="../../../assets/Tourimage/asset 92.jpg"
                        ></v-img>
                </span>
            </v-avatar>
            <h5>Hosted by</h5>
            <p>3 Hours</p>    
        </v-col> <!--icons-->

        <v-col class="px-6" md="2" lg="2" xl="2" cols="4">
            <v-avatar color="white" size="62">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 93.jpg"
                    ></v-img>
            </span>
            </v-avatar>
                
            <h5>Hosted by</h5>
            <p>3 Hours</p>    
        </v-col> <!--icons-->

        <v-col class="px-6" md="2" lg="2" xl="2" cols="4">
            <v-avatar color="white" size="62">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 94.jpg"
                    ></v-img>
            </span>
            </v-avatar>
            <h5>Hosted by</h5>
            <p>3 Hours</p>    
        </v-col> <!--icons-->
            
      </v-row>
  </v-container>
</template>

<script>
export default {
data:()=>({
    users:[
        {
            name:'name1'
        },
        {
            name:'name1'
        },
        {
            name:'name1'
        },
        {
            name:'name1'
        },
        {
            name:'name1'
        },
        {
            name:'name1'
        }
    ]
})
}
</script>

<style>
.blueTxt{
    color: rgb(28, 182, 230)!important;
}
.bgLiteBlue{
 background-color: #f0f5f7;
 border-radius:4px;
 
}
</style>