<template>
  <v-container fluid class="pa-0">
      <v-container class="childContainer">
        <v-row>
            <v-col md="8" lg="8" xl="8" cols="12">
                <messenger/>
                <youtubeSec/>
                <itinerary/>
            </v-col><!--Mother Col 1-->
            <v-col cols="4" class="hidden-sm-and-down">
                <v-banner class="pr-4" style="border: 1px solid rgb(226, 236, 240); border-radius: 6px; top:60px!important;" width="100%" sticky>
                    <v-row>
                        
                        <v-col cols="12">
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
                        
                        <v-col cols="12" class="d-flex py-2 my-0">
                            <h5 class="mx-2">Adults</h5>
                            <v-spacer></v-spacer>
                            <v-btn class=" addBtn " outlined color="teal">
                                <v-icon >mdi-minus</v-icon>
                            </v-btn>
                            <p class="my-2"> 10 </p>
                            <v-btn class="addBtn" outlined color="teal">
                                <v-icon>mdi-plus</v-icon>
                            </v-btn>
                        </v-col><!--Adults-->

                        <v-col cols="12" class="d-flex py-2 my-0">
                            <h5>Children</h5>
                            <v-spacer></v-spacer>
                            <v-btn class="addBtn" outlined color="teal">
                                <v-icon>mdi-minus</v-icon>
                            </v-btn>
                            <p class="my-2"> 10 </p>
                            <v-btn class="addBtn" outlined color="teal">
                                <v-icon>mdi-plus</v-icon>
                            </v-btn>
                        </v-col><!--Children-->
                        <hr>
                        <v-col cols="12" class="d-flex py-1 my-0">
                         <p>USD 34.88 x 2 adults</p> <v-spacer/> <p>USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="12" class="d-flex py-1 my-0">
                            <p>Booking fee + tax</p> <v-spacer/> <p>USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="12" class="d-flex py-2 my-0">
                            <p>Accident Insurance</p> <v-spacer/> <p color="teal">FREE</p>
                        </v-col>
                        
                        <v-col cols="12" class="d-flex py-2 my-0">
                            <h5>Total</h5> <v-spacer/> <p>USD 69.75</p>
                        </v-col>
                        
                        <v-col cols="12" class="d-flex py-0 my-0">
                            <v-spacer/> <p>100% Satisfaction guaranteed</p>
                        </v-col>
                        <v-btn dense class="mx-2 white--text" style="padding: 0 114px;
                        margin-left: 13px!important;"  width="90%" color="green darken-3">
                        50 reviews </v-btn>
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
// import explore from './StrFoodComponents/Explore'
// import PriceMeetingPoint from './StrFoodComponents/Price-to-MeetingPoint'
// import reviews from './StrFoodComponents/Reviews'
export default {
    components:{
        messenger,
        youtubeSec,
        itinerary,
        // explore,
        // PriceMeetingPoint,
        // reviews

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
</style>