<template>
  <v-container>
      <v-row class="pt-12 mt-12 mx-6">
          <div class="backgroundTMT">
          <v-col cols="8" class="px-8 white--text">
              <h2 class="headtxt py-5">What’s a Day Like with TakeMeTour?</h2>
              <p>Unlike others, all tours are led by true Local Experts. They’ll open your eyes to see much more than what your typical guidebooks suggest. 
                  Book any tour & be one with the locals. It’s a lifetime experience you simply can’t find anywhere else!
              </p>
              <p>
                  Tell me more
              </p>
          </v-col>

          <v-col cols="4" class="mb-0 pa-0">
              <v-row>
              <v-col class="imagesTMT pl-0" >
                  <v-img 
                    class="white--text align-end"
                    height="100%"
                    width="100%"
                    src="../assets/images/asset 41.png"
                    >
                    </v-img>
              </v-col>
              </v-row>
              
          </v-col>
          </div>
      </v-row>
  </v-container>
</template>

<script>
export default {
    data:()=>({
    })
}
</script>

<style>
    .backgroundTMT{
        max-width: 100%!important;
        display: flex;
        flex: 1 1 auto;
        flex-wrap: wrap;
        background-color: #FF7923;
        border-radius: .35rem;
    }
    .imagesTMT{
        margin-top: -17px;
        padding-bottom: 0;
    }
    .headtxt{
        width: 34%;
    }
</style>