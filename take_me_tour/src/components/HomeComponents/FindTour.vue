<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container class="childContainer">
      <v-row class="pt-12 mt-12 mx-md-6 mx-lg-6 mx-xl-6 mx-1">
          <div class="background">
          <v-col cols="6">
              <h2 class="findTxt">Find the right tour for you</h2>
              <v-col width="auto">
                    <v-btn max-width="172" max-height="39" :ripple="false" height="40" class="srcBtn pl-3 pr-0" style="text-transform:unset!important;">Try this quiz! <v-icon class="px-1">mdi-chevron-right</v-icon> </v-btn>
              </v-col>
          </v-col>

          <v-col md="4" lg="6" xl="6" cols="6" class="mb-0 pb-0">
              <v-row>
              <v-col class="images hidden-sm-and-down" md="4" lg="4" xl="4" cols="12">
                  <v-img 
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    src="../../assets/images/asset 29.png"
                    >
                    </v-img>
              </v-col>
              <v-col class="images" md="4" lg="4" xl="4" cols="12" >
                  <v-img 
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    src="../../assets/images/asset 30.png"
                    >
                    </v-img>
              </v-col>
              <v-col class="images hidden-sm-and-down" md="4" lg="4" xl="4" cols="12" >
                  <v-img 
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    src="../../assets/images/asset 31.png"
                    >
                    </v-img>
              </v-col>
              </v-row>
              
          </v-col>
          </div>
      </v-row>
  </v-container>
</v-container>
</template>

<script>
export default {
}
</script>

<style>
    .background{
        max-width: 100%!important;
        display: flex;
        flex: 1 1 auto;
        flex-wrap: wrap;
        background-color: #DDF2F8;
        border-radius: .35rem;
        padding: 15px 10px;
    }
    .images{
        margin: -90px -15px;
        padding-bottom: 0;
    }
    .findTxt{
        font-size: 20px;
        color: #4d4d5b;
        margin-left: 11px;
        font-weight: 500;
    }
    .srcBtn{
            width: fit-content;
            padding: 8px 12px!important;
            font-weight: 600;
            border-radius: 8px!important;
            background: rgb(255, 121, 35)!important;
            color: #ffffff!important;
            font-size: 15px!important;
    }
    
    @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .images {
            margin: -86px 0px;
            padding-bottom: 0;
        }
        .findTxt{
            font-size: 14px;
            font-weight: 300;
        }
        .srcBtn{
            padding: 0px 15px!important;
            margin: 0px -14px;
        }
    }
</style>