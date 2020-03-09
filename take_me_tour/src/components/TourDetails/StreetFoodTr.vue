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
                <v-banner style="border: 1px solid rgb(226, 236, 240); border-radius: 6px; top:60px!important;" width="94%" sticky>
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
                        
                        <v-col cols="11" class="d-flex py-2 my-0">
                            <h5 class="mx-2">Adults</h5>
                            <v-spacer></v-spacer>
                            <v-btn min-width="44" class=" addBtn px-2 " outlined color="teal">
                                <v-icon >mdi-minus</v-icon>
                            </v-btn>
                            <p class="my-2"> 10 </p>
                            <v-btn min-width="44" class="addBtn px-2" outlined color="teal">
                                <v-icon>mdi-plus</v-icon>
                            </v-btn>
                        </v-col><!--Adults-->

                        <v-col cols="11" class="d-flex py-2 my-0">
                            <h5>Children</h5>
                            <v-spacer></v-spacer>
                            <v-btn min-width="44" class="addBtn px-2" outlined color="teal">
                                <v-icon>mdi-minus</v-icon>
                            </v-btn>
                            <p class="my-2"> 10 </p>
                            <v-btn min-width="44" class="addBtn px-2" outlined color="teal">
                                <v-icon>mdi-plus</v-icon>
                            </v-btn>
                        </v-col><!--Children-->

                        <v-col cols="11" class="d-flex py-1 my-0">
                         <p>USD 34.88 x 2 adults</p> <v-spacer/> <p>USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-1 my-0">
                            <p>Booking fee + tax </p>
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
                             <v-spacer/> <p>USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-2 my-0">
                            <p>Accident Insurance</p> <v-spacer/> <h6 class="GreenTxt">FREE</h6>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-2 my-0">
                            <h5>Total</h5> <v-spacer/> <h5  class="GreenTxt" >USD 69.75</h5>
                        </v-col>
                        
                        <v-col cols="11" class="d-flex py-0 my-0">
                            <v-spacer/> <p>100% Satisfaction guaranteed</p>
                        </v-col>
                        <v-btn dense class="mx-2 white--text" style="padding: 0 114px;
                        margin-left: 13px!important; background-color:#32D672"  width="86%">
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
        margin: 0 8px !important;
        max-width: 48px!important;
        
    }
    .GreenTxt{
        font-weight: 700!important;
        color: rgb(50, 214, 114)!important;
        font-size: 14px;
    }
    .InfoDiv .v-menu__content {
        margin-left: -76px!important;
    }

</style>