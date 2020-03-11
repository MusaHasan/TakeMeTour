<template>
<v-container fluid class="pa-0 BodyBGcolot">
    <v-container class="childContainer">
      <v-row >
          <h2 class="TitelTxt mb-6">Tour Available Tomorrow</h2>
        <v-sheet
          class="mx-auto transparent "
          max-width="100%"
        >
          <v-slide-group
            class="pa-2 sliderContainer" 
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
              class=" sliderImgCrd "
            >
                <v-card
                    class="white TurAvCrd"
                    max-width="min-content"
                    max-height="370"
                    
                >
                    <v-img
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    :src="require(`../../assets/images/${image.name}`)"
                    >
                    <v-icon class="heartIc">mdi-heart-outline</v-icon>
                    </v-img>

                    <v-card-subtitle class="tagTxt">Bangkok</v-card-subtitle>

                    <v-card-text style="margin: -9px 0;" class="text--primary">
                    <div><h4 style="font-size:16px;color: #4D4D5B!important;font-weight: 600;">5 famous Temples & Street Food at Wang Lang... </h4></div>

                    <p class="mb-0" style="font-size: 14px!important;">Whitsunday Island, Whitsunday..</p>
                    <v-row>
                      <v-col cols="5">
                        <div class="d-flex reatingStar">
                            <v-rating
                            color="yellow darken-3"
                            background-color="yellow darken-3"
                            empty-icon="$ratingFull"
                          ></v-rating>(114)
                        </div>
                        
                        <p class="timeTxt"><v-icon small>mdi-clock-outline</v-icon> 08:00- 19:00</p>
                      </v-col>
                      <v-spacer/>
                      <v-col cols="6">
                        <p class="caption mt-4" > <span class=" green--text">USD 88.85</span> / <span class="personTxt">person</span> </p>
                      </v-col>
                    </v-row>
                    </v-card-text>

                </v-card>
        
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
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
            {
                name:'asset 21.jpg', label:'asset 11.png', route:''
            },
            {
                name:'asset 22.jpg', label:'asset 12.png', route:''
            },
            {
                name:'asset 25.png', label:'asset 12.png', route:''
            },
            {
                name:'asset 27.png', label:'asset 12.png', route:''
            },
            {
                name:'asset 27.png', label:'asset 12.png', route:''
            }

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
  .TurAvCrd{
    border-radius: 6px!important;
    box-shadow: rgba(0, 0, 0, 0.06) 0px 1px 5px 0px!important;
    cursor: pointer;
  }
  .heartIc{
    position: relative!important;
    top: -175px;
    left: 239px;
    color: white!important;
  }
  .tagTxt{
    position: relative;
    top: -18px;
    color:#1cb6e6!important;
    background-color: aliceblue;
    width: fit-content!important;
    padding: 6px 13px;
    font-size: 12px!important;
    border-radius: 0 50px 50px 0;
  }
  .reatingStar .v-rating .v-icon{
    font-size: 12px!important;
  }
  .personTxt{
    font-size: 9px!important;
  }
  .timeTxt{
    font-size: 10px!important;
  }
  .sliderImgCrd{
    margin: 0 5px;
  }
  @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
      .TurAvCrd{
        width: 273px!important;
        height: 370px!important;
      }
    }

</style>
