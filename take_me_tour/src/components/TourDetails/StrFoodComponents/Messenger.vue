<template>
  <v-container>
      <v-row class="hidden-sm-and-down">
          <p class="navigateTxt">Home <v-icon style="width:5px;" size="17">mdi-chevron-right</v-icon> Bangkok <v-icon style="width:5px;" size="17">mdi-chevron-right</v-icon> Street Food Tour in Bangkok Chinatown</p>
      </v-row>
       <v-row class="hidden-md-and-up mt-3">
            <v-col cols="5">
                <v-row class="mx-1">
                    <v-col class="pa-0" cols="4">
                    <v-card
                            class="mx-0 text-center"
                            tile
                            max-width="36"
                            max-height="32"
                        >
                            <p style="font-size:9px!important; background-color:rgb(22, 196, 100)!important " class="mb-0 white--text">MAR</p>
                            <p style="font-size:13px!important"><v-icon color="orange darken-3" style="font-size:13px!important">mdi-flash</v-icon>12</p>
                        </v-card>
                    </v-col>
                    <v-col class="pa-0" cols="4">
                    <v-card
                            class="mx-0 text-center"
                            tile
                            max-width="36"
                            max-height="32"
                        >
                            <p style="font-size:9px!important; background-color:rgb(22, 196, 100)!important " class="mb-0 white--text">MAR</p>
                            <p style="font-size:13px!important"><v-icon color="orange darken-3" style="font-size:13px!important">mdi-flash</v-icon>13</p>
                        </v-card>
                    </v-col>
                    <v-col class="pa-0" cols="4">
                    <v-card
                            class="mx-0 text-center"
                            tile
                            max-width="36"
                            max-height="32"
                        >
                            <p style="font-size:9px!important; background-color:rgb(22, 196, 100)!important " class="mb-0 white--text">MAR</p>
                            <p style="font-size:13px!important"><v-icon color="orange darken-3" style="font-size:13px!important">mdi-flash</v-icon>14</p>
                        </v-card>
                    </v-col>
                </v-row>
            </v-col>
            <v-col cols="7"></v-col>
        </v-row>
      <v-row>
          <v-col class="pt-1 pt-md-9 pt-lg-9 pt-xl-9 pb-0" md="8"  lg="8" xl="8" cols="12">
              <h3 class="d-inline">Street Food Tour in Bangkok Chinatown</h3> 
          </v-col>
          <v-col cols="2"><v-btn class="ma-2 hidden-sm-and-down" text color="indigo"><v-icon>mdi-briefcase-upload-outline</v-icon> Share</v-btn></v-col>
          <v-col cols="2"><v-btn class="ma-2 hidden-sm-and-down" text color="indigo"><v-icon>mdi-heart-outline</v-icon> Wishlist</v-btn></v-col>
      </v-row><!--Street Food Title share, wishlist ICon-->
      <v-row>
          <v-col cols="12" class="d-flex py-0">
            <v-img class="mx-3 " max-width="92" max-height="22" src="../../../assets/Tourimage/asset 11.png"></v-img> <span class="blueTxt">Bangkok</span> 
          </v-col>

          <v-col md="12" lg="12" xl="12" cols="6" class="d-flex pt-0 pb-2">
                <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating>
                <v-btn class="ma-2 px-2 white--text" height="33" color="rgb(50, 214, 114)">50 reviews <v-icon>mdi-chevron-right</v-icon></v-btn>
          </v-col>
      </v-row>
      <v-row class="bgLiteBlue"> <!--Massage section-->
          <v-col class="py-0" cols="12">
              <v-row>
                  <v-col class="imgAvater" md="2" lg="2" xl="2" cols="2">
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
                  <v-col class="py-0 pr-0 mt-5 msTxt" md="8" lg="8" xl="8" cols="7">
                      <p class="my-0">Local Experience by</p>
                      <p style="color:#16c464!important;">Selected Local Experts</p>
                  </v-col> <!--middel Text-->
                  
                  <v-col class="py-0 px-0" md="2" lg="2" xl="2" cols="2">
                    <p class="blueTxt my-5"><v-icon class="ml-4 ml-md-0 ml-lg-0 ml-xl-0" color="rgb(28, 182, 230)">mdi-comment-text-multiple-outline</v-icon> Massage</p>
                  </v-col><!--Massage Text & Icon-->
              </v-row>
          </v-col>

      </v-row>
      <v-row >

        <v-col class="ml-md-10 ml-lg-10 ml-xl-10 mr-md-3 mr-lg-3 mr-xl-3 px-6 text-center" md="2" lg="2" xl="2" cols="4">
            <v-avatar color="white" class="mt-6" size="35">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 90.jpg"
                    ></v-img>
            </span>
            </v-avatar>
            <h5 class="iconName">Hosted by locals</h5>    
        </v-col> <!--icons-->

        <v-col class="pl-2"  md="2" lg="2" xl="2" cols="4">
            <v-avatar class="mx-9 mt-6" color="white" size="35">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 91.jpg"
                    ></v-img>
            </span>
            </v-avatar>
            <div class="text-center">
            <h5 class="iconName">Hosted by</h5>
            <p>3 Hours</p>
            </div>    
        </v-col> <!--icons-->

        <v-col class="pl-2"  md="2" lg="2" xl="2" cols="4">
            <v-avatar class="mx-9 mt-6" color="white" size="35">
                <span class="white--text headline">
                    <v-img
                            class="elevation-0"
                            src="../../../assets/Tourimage/asset 92.jpg"
                        ></v-img>
                </span>
            </v-avatar>
            <div class="text-center">
            <h5 class="iconName">Vehicle</h5>
            <p>Private Car</p> 
            </div>   
        </v-col> <!--icons-->

        <v-col class="pl-2"  md="2" lg="2" xl="2" cols="4">
            <v-avatar class="mx-9 mt-6" color="white" size="35">
            <span class="white--text headline">
                <v-img
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 93.jpg"
                    ></v-img>
            </span>
            </v-avatar>
             <div class="text-center">  
                <h5 class="iconName">Free</h5>
                <p>Hotel Pickup</p>
             </div>    
        </v-col> <!--icons-->

        <v-col class="pl-2"  md="2" lg="2" xl="2" cols="4">
            <v-avatar class="mx-9 mt-6" color="white" size="35">
            <span class="white--text headline">
                <v-img 
                        class="elevation-0"
                        src="../../../assets/Tourimage/asset 94.jpg"
                    ></v-img>
            </span>
            </v-avatar>
            <div class="text-center">
                <h5 class="iconName">Hosted In</h5>
                <p>English, ไทย</p> 
            </div>  
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
.imgAvater{
     padding: 8px 44px !important;
}
.msTxt{
    margin-left: -17px;
}
.navigateTxt{
    font-size: 12px!important;
    margin-left: 10px;
    margin-bottom: -18px!important;
}
.iconName{
    font-weight: 600;
    font-family: sans-serif;
    font-size: 15px;
    color: #425e6c;
}
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
    .imgAvater{
        padding: 0 12px!important;
        margin: 10px 12px
    }
    .msTxt{
        margin-left: -16px;
}
}
</style>