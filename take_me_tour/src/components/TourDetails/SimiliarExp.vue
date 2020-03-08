<template>
<v-container fluid class="pa-0 BodyBGcolot">
    <v-container class="childContainer">
      <h3>Tour Available Tomorrow</h3>
      <v-row >
            <v-col md="3" lg="3" xl="3" cols="12" class="mb-2" 
                v-for="(image,i) in images" :key="i">
                <v-card
                    class="white SimilarCrd"
                    max-width="min-content"
                    max-height="370"
                >
                    <v-img
                    class="white--text align-end"
                    height="206px"
                    width="343px"
                    :src="require(`../../assets/images/${image.name}`)"
                    >
                    <v-icon class="SimilheartIc">mdi-heart-outline</v-icon>
                    </v-img>

                    <v-card-subtitle class="tagTxt">Number 10</v-card-subtitle>

                    <v-card-text class="text--primary">
                    <div><h4>5 famous Temples & Street Food at Wang Lang... </h4></div>

                    <div>Whitsunday Island, Whitsunday..</div>
                    <v-row>
                      <v-col cols="5">
                        <div class="d-flex">
                            <v-rating
                            color="yellow darken-3"
                            background-color="yellow darken-3"
                            empty-icon="$ratingFull"
                            small
                          ></v-rating>(114)
                        </div>
                        
                        <p class="timeTxt"><v-icon>mdi-clock-outline</v-icon> 08:00- 19:00</p>
                      </v-col>
                      <v-spacer/>
                      <v-col cols="6">
                        <p class="caption mt-4" > <span class=" green--text">USD 88.85</span> / <span class="personTxt">person</span> </p>
                      </v-col>
                    </v-row>
                    </v-card-text>

                </v-card>
            </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
// @ is an alias to /src


export default {
    data:()=>({
        images:[
            {
                name:'asset 13.png', label:'asset 7.png', route:'' 
            },
            {
                name:'asset 15.png', label:'asset 8.png', route:''        
            },
            {
                name:'asset 16.jpg', label:'asset 9.png', route:''            
            },
            {
                name:'asset 17.png', label:'asset 10.png', route:''
            },
        ]
    })
  
}
</script>
<style >
  .v-slide-group__prev, .v-slide-group__next{
    flex: 0 1 34px!important;
    min-width: 27px!important;
    background-color: #fffafa00;
  }
  .SimilarCrd{
    border-radius: 6px!important;
    box-shadow: rgba(0, 0, 0, 0.06) 0px 1px 5px 0px!important;
    cursor: pointer;
  }
  .tagTxt{
    position: relative;
    top: -18px;
    color:#1cb6e6!important;
    background-color: aliceblue;
    width: fit-content!important;
    padding: 8px 13px;
    border-radius: 0 50px 50px 0;
  }
  .SimilheartIc{
    top: -171px;
    right: -233px;
    color: white!important;
  }
  @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
      .SimilarCrd{
        width: 343px!important;
        height: 370px!important;
      }
      .SimilheartIc{
        top: -171px;
        right: -310px;
        color: white!important;
      }
    }

</style>
