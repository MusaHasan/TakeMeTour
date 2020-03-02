<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container>
      <v-row class="pt-12 mt-12 mx-6">
          <div class="background">
          <v-col cols="6">
              <h2>Find the right tour for you</h2>
              <v-col width="auto">
                    <v-btn max-width="150" max-height="48" height="48" class="searchBtn" color="orange darken-3" dark>Try this quiz!</v-btn>
              </v-col>
          </v-col>

          <v-col cols="6" class="mb-0 pb-0">
              <v-row>
              <v-col class="images" cols="4" v-for="(image,i) in images" :key="i">
                  <v-img 
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    :src="require(`../../assets/images/${image.name}`)"
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
        images:[
            {
                name: "asset 29.png"  
            },
            {
                name: "asset 30.png"  
            },
            {
                name: "asset 31.png"  
            }
        ]
    })
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
    }
    .images{
        margin: -90px -15px;
        padding-bottom: 0;
    }
    .BodyBGcolot{
        background-color: #F8FBFB;
    }
</style>