<template>
  <v-container fluid class="pa-0">
      <v-container class="childContainer">
        <v-row>
            <v-col class="pa-md-4 pa-lg-4 pa-xl-4 pa-1" md="8" lg="8" xl="8" cols="12">
                 <messenger/>
                 <youtubeSec/>
                <itinerary/><!--done-->
                <explore/>
                <PriceMeetingPoint/>
                <reviews/>
            </v-col><!--Mother Col 1-->
            <v-col cols="4" class="hidden-sm-and-down">
                <v-banner class="instantBookBtn" style="border: 1px solid rgb(226, 236, 240); border-radius: 6px; top:60px!important;" width="90%" sticky>
                    <v-row>
                        
                        <v-col cols="11">
                            <v-menu
                            v-model="menu1"
                            :close-on-content-click="false"
                            max-width="100%"
                            :outlined="color='rgb(226, 236, 240)'"

                            >
                            <template v-slot:activator="{ on }">
                                <v-text-field
                                :value="computedDateFormattedMomentjs"
                                append-icon="mdi-chevron-down"
                                readonly
                                outlined
                                v-on="on"
                                @click:clear="date = null"
                                > </v-text-field>
                            </template>
                            <v-date-picker
                                v-model="date"
                                @change="menu1 = false"
                            ></v-date-picker>
                            </v-menu>
                        </v-col><!--Date-->
                        
                        <v-col cols="11" class="d-flex pt-4 pb-0 my-0">
                            <h5 class="mt-1 mx-3">Adults</h5>
                            <v-spacer></v-spacer>
                            <v-btn min-width="32" height="32" class=" addBtn " outlined color="rgb(66, 94, 108)">
                                <v-icon >mdi-minus</v-icon>
                            </v-btn>
                            <p class="my-2"> 10 </p>
                            <v-btn min-width="32" height="32" class="addBtn" outlined color="rgb(66, 94, 108)">
                                <v-icon>mdi-plus</v-icon>
                            </v-btn>
                        </v-col><!--Adults-->

                        <v-col cols="11" class="d-flex py-2 my-0">
                            <div>
                                <h5 class=" mt-1 mx-3">Children</h5>
                                <p style="font-size:10px!important" class=" my-0  mx-3">Age 2-12</p>
                            </div>
                            <v-spacer></v-spacer>
                            <v-btn min-width="32" height="32" disabled class="addBtn" outlined color="rgb(66, 94, 108)">
                                <v-icon>mdi-minus</v-icon>
                            </v-btn>
                            <p class="my-2"> 10 </p>
                            <v-btn min-width="32" height="32" class="addBtn" outlined color="rgb(66, 94, 108)">
                                <v-icon>mdi-plus</v-icon>
                            </v-btn>
                        </v-col><!--Children-->

                        <v-col cols="11" class="py-0 my-1" style="border-bottom: 1px solid rgb(226, 236, 240)"></v-col>

                        <v-col cols="11" class="d-flex py-1 my-0">
                         <p class="mb-0">USD 34.88 x 2 adults</p> <v-spacer/> <p class="mb-0">USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-1 my-0">
                            <p class="mb-0">Booking fee + tax </p>
                                <div class="text-center">
                                    <v-menu offset-y>
                                        <template v-slot:activator="{ on }">
                                            <v-btn tile large icon height="20" width="20"
                                            v-on="on"
                                            >
                                            <v-icon small color="red" >mdi-information-outline</v-icon>
                                            </v-btn>
                                        </template>
                                        <v-list class="InfoDiv" width='200'>
                                            <v-list-item >
                                                <h6> Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis, </h6> 
                                            </v-list-item>
                                        </v-list>
                                    </v-menu>
                                </div>
                             <v-spacer/> <p class="mb-0">USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-2 my-0">
                            <p class="mb-0">Accident Insurance</p> <v-spacer/> <h6 class="GreenTxt mb-0">FREE</h6>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-2 my-0">
                            <h5>Total</h5> <v-spacer/> <h5  class="GreenTxtUSD" >USD 69.75</h5>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-0 my-0">
                            <v-spacer/> <p style="font-size:13px!important">100% Satisfaction guaranteed</p>
                        </v-col>
                        <v-btn dense class="mx-2 white--text" style="padding: 0 114px;
                        margin-left: 13px!important; font-weight: 700; font-size: 15px; background-color:rgb(22, 196, 100)"  width="84%">
                        Instant Book </v-btn>
                    </v-row>
                </v-banner>
            </v-col><!--Mother Col 2-->
        </v-row>
      </v-container>
  </v-container>
</template>

<script>
import moment from 'moment'
import messenger from './StrFoodComponents/Messenger'
import youtubeSec from './StrFoodComponents/youtubeVideo'
import itinerary from './StrFoodComponents/Itinerary'
import explore from './StrFoodComponents/Explore'
import PriceMeetingPoint from './StrFoodComponents/Price-to-MeetingPoint'
import reviews from './StrFoodComponents/Reviews'
export default {
    components:{
        messenger,
        youtubeSec,
        itinerary,
        explore,
        PriceMeetingPoint,
        reviews

    },
    data: () => ({
      date: new Date().toISOString().substr(0, 10),
      menu1: false,
      menu2: false,
    }),

    computed: {
      computedDateFormattedMomentjs () {
        return this.date ? moment(this.date).format('Do MMMM YYYY') : ''
      }
    },

}
</script>

<style>
    .v-input__append-inner{
        padding: 10px!important;
    }
    .addBtn{
        margin: 4px 8px !important;
        max-width: 32px!important;
        
    }
    .GreenTxt{
        font-weight: 600!important;
        color: rgb(50, 214, 114)!important;
        font-size: 14px;
    }
    .GreenTxtUSD{
       font-weight: 600!important;
        color: rgb(50, 214, 114)!important;
        font-size: 16px; 
    }
    .InfoDiv .v-menu__content {
        margin-left: -76px!important;
    }
    .instantBookBtn .v-banner__wrapper {
        padding: 16px 8px 16px 13px!important;
    }

</style>