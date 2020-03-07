<template>
    <v-container fluid class="pa-0 BodyBGcolot">
        <v-container class="childContainer">
            <v-row class="NotExacRow">
                <v-col class="notExacTxt" md="7" lg="7" xl="7" cols="12">
                    <div class="bdr">
                        <h3 class="mb-6">Not Exactly What You’re Looking For?</h3>
                        <p>Customize existing trips the way you want or even tell us where you want to go! 
                            We’ll find a Local Expert to take you there.</p>
                        <v-btn class="ma-2 white--text" color="indigo">Send Request</v-btn>
                    </div>
                </v-col>
                <v-col class="sideImage pa-0" md="5" lg="5" xl="5" cols="12">    
                    <v-img max-width="100%" max-height="290" aspect-ratio="1.7" src="../../assets/Tourimage/asset 88.jpeg"></v-img> 
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
.NotExacRow{
    margin: 1px 2px;
    background-color: #F0F5F8 ;
}
.bdr{
    border-radius: 14px;
}
.notExacTxt{
    padding: 24px 32px ;
}
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px){
    .sideImage{
        position: absolute;
        z-index: 0;
        margin: -6px -3px
    }
    .notExacTxt{
        z-index: 1;
        background-color: rgba(240, 245, 248, 0.671)!important;
        padding: 36px 2px;
        margin: -36px 14px;
    }
}
</style>