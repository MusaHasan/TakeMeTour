<template>
    <v-container fluid class="pa-0">
        <v-container class="childContainer">
            <v-row class="NotExacRow hidden-sm-and-down">
                <v-col class="notExacTxt" md="7" lg="7" xl="7" cols="12">
                    <div class="bdr">
                        <h3 class="mb-6">Not Exactly What You’re Looking For?</h3>
                        <p>Customize existing trips the way you want or even tell us where you want to go! 
                            We’ll find a Local Expert to take you there.</p>
                        <v-btn style="border-radius: 6px;" class="ma-2 white--text" color="rgb(28, 182, 230)">Send Request</v-btn>
                    </div>
                </v-col>
                <v-col class="sideImage pa-0" md="5" lg="5" xl="5" cols="12">
                      
                    <v-img max-width="100%" max-height="290" aspect-ratio="1.7" src="../../assets/Tourimage/asset 88.jpeg"></v-img> 
                </v-col>
            </v-row>


            <v-row class="NotExacRow hidden-md-and-up">
                 <v-col class="sideImage pa-0" md="5" lg="5" xl="5" cols="12">
                    <v-img max-width="100%" max-height="290" aspect-ratio="1.7" src="../../assets/Tourimage/asset 88.jpeg">
                        <v-col class="notExacTxt" md="7" lg="7" xl="7" cols="12">
                            <div class="bdr">
                                <h3 class="mb-6">Not Exactly What You’re Looking For?</h3>
                                <p>Customize existing trips the way you want or even tell us where you want to go! 
                                    We’ll find a Local Expert to take you there.</p>
                                <v-btn class="ma-2 white--text" color="blue darken-1">Send Request</v-btn>
                            </div>
                        </v-col>
                    </v-img> 
                </v-col>
            </v-row>
        </v-container>
    </v-container>
</template>

<script>
export default {

}
</script>

<style>
.bdr{
    border-radius: 14px;
    margin: -12px -47px -13px 0px;
    padding: 62px 72px;
    background-color: #F0F5F8 ;
}

.sideImage .v-image__image--cover{
    border-radius: 10px;
}
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px){
    .NotExacRow{
        margin: 1px 2px;
        background-color: #F0F5F8 ;
    }
    .bdr{
        border-radius: 14px;
        margin: -12px -47px -13px 0px;
        padding: 0;
        background-color: rgba(240, 245, 248, 0) ;
    }
    .notExacTxt{
        padding: 55px 52px;
    }
    .sideImage{
        z-index: 1;
        width: 93%!important;
    }
    .sideImage .v-responsive__sizer{
       padding-bottom: 65.8235%!important; 
    }
    .notExacTxt{
        z-index: 1;
        background-color: rgba(240, 245, 248, 0.671)!important;
        margin: -8px 0;
    }
}
</style>