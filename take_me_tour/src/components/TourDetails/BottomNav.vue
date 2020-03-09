<template>
    <v-container fluid>
        <v-bottom-navigation
            class="hidden-lg-and-up"
            scroll-target="#scroll-area-1"
            hide-on-scroll
            fixed
            horizontal
            >
            <v-row>
                <v-col cols="6">
                    <p class="UsdTxt"> <span class=" ml-6 green--text">USD 88.85</span> / <span class="personTxt">person</span> </p>
                    <div class="reatingStar ml-6 ">
                        <v-rating
                        color="yellow darken-3"
                        background-color="yellow darken-3"
                        empty-icon="$ratingFull"
                        ></v-rating> <span style="font-size:9px!important">(114)</span> 
                    </div>
                </v-col>
                <v-col cols="6">
                    <v-btn class="mx-3 body-2 font-weight-light white--text text-capitalize " max-width="145" width="145" max-height="40" height="40" tile style="background-color:#21D366">Book</v-btn>
                </v-col>
            </v-row>
                

            
        </v-bottom-navigation>
    </v-container>
</template>
<style >
    .UsdTxt{
        margin-bottom: -4px!important;
    }
</style>