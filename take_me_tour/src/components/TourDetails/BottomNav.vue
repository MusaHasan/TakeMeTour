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
                <v-col cols="8">
                    <p class="UsdTxt"> <span class=" ml-6 green--text">USD 88.85</span> / <span class="personTxt">person</span> </p>
                    <div class="reatingStar d-flex ml-6 ">
                        <v-rating
                        color="yellow darken-3"
                        background-color="yellow darken-3"
                        empty-icon="$ratingFull"
                        ></v-rating> <span class="ma-2" style="font-size:9px!important;">(114)</span> 
                    </div>
                </v-col>
                <v-col cols="4">
                    <v-btn class=" BookBtn"><span style="color: white!important">Book</span> </v-btn>
                </v-col>
            </v-row>
                

            
        </v-bottom-navigation>
    </v-container>
</template>
<style >
    .UsdTxt{
        margin-bottom: -4px!important;
    }
    .BookBtn{
        height: 40px!important;
        max-height: 36px!important;
        max-width: 100px!important;
        border-radius: 6px!important;
        font-weight: 700!important;
        margin-left: -20px;
        font-size: 16px!important;
        width: 100px!important;
        background-color: rgb(33, 211, 102)!important;
    }
</style>