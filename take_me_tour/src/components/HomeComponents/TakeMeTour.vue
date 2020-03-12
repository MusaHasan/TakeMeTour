<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container class="childContainer Con-orengBg">
      <v-row class="pt-12 mt-12 orengBg">
          <div class="backgroundTMT">
          <v-col md="8" lg="8" xl="8" cols="12" class="px-8 white--text">
              <h2 class="headtxt py-5 px-md-0 px-lg-0 px-xl-0 px-4">What’s a Day Like with <span class="headTxtFocus">TakeMeTour?</span> </h2>
              <p class="bodytxt">Unlike others, all tours are led by true Local Experts. They’ll open your eyes to see much more than what your typical guidebooks suggest. 
                  Book any tour & be one with the locals. It’s a lifetime experience you simply can’t find anywhere else!
              </p>
              <p class="bodytxt mb-0">
                  Tell me more <v-icon color="white">mdi-chevron-right</v-icon>
              </p>
          </v-col>

          <v-col md="" lg="4" xl="4" cols="12" class="mb-0 pa-0">
              <v-row>
              <v-col class="imagesTMT pl-0" >
                  <v-img 
                    class="white--text align-end"
                    height="100%"
                    width="100%"
                    src="../../assets/images/asset 41.png"
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
    data:()=>({
    })
}
</script>

<style>
    .orengBg{
        margin-left: 12px;
        margin-right: 12px;
    }
    .backgroundTMT{
        max-width: 100%!important;
        display: flex;
        flex: 1 1 auto;
        flex-wrap: wrap;
        background-color: #FF7923;
        border-radius: .35rem;
    }
    .imagesTMT{
        margin-top: -25px;
        padding-bottom: 0;
    }
    .headtxt{
        width: 34%;
    }
    .bodytxt{
        color: white!important;
    }
     @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .imagesTMT{
            margin-top: -17px;
            padding-bottom: 0;
             
        }
        .imagesTMT .v-image{
            width: 60%!important;
            margin-left: 155px;
        }

        .headtxt{
            width: 100%;
            text-align: center

        }
        .headTxtFocus{
            font-size: 30px;
        }
        .bodytxt{
            text-align: center;
            padding: 0 13px;
            font-weight: 600!important;
            line-height: 18px!important;
            font-size: 14px!important;
        }
        .orengBg{
            margin-left: 0;
            margin-right: 0;
            
        }
        .Con-orengBg{
            padding: 0!important;
        }
    }
</style>