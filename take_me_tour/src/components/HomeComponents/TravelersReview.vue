<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container class="childContainer">
      <v-row >
          <h2 class="TitelTxt mb-6">Traveler's Reviews</h2>
        <v-sheet
          class="mx-auto mb-8 transparent"
          elevation="0"
          max-width="100%"
        >
          <v-slide-group
            class="pa-0 sliderContainer"
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
              class="ml-2 reviewsCrd"
            >
              <v-card
                class="ma-1 TrvRevCrd"
                height="180"
                width="363"
                elevation="0"
                :ripple="false"
              >
                <v-row>
                    <v-list-item class="grow">
                    <v-col cols="2"> 
                         <v-list-item-avatar color="grey darken-3">
                            <v-img
                                class="elevation-6"
                                :src="require(`../../assets/images/${image.avatar}`)"
                            ></v-img>
                        </v-list-item-avatar>
                    </v-col>
                    <v-col md="6" lg="6" xl="6" cols="4">
                        <v-list-item-content style="width:130px" >
                            <v-list-item-title class="userName">{{image.name}}</v-list-item-title>
                             <v-list-item-subtitle > 
                                    <v-img
                                        class="white--text d-inline-block"
                                        height="20"
                                        width="30"
                                        :src="require(`../../assets/images/${image.flag}`)"
                                    >
                                    </v-img> <span class="flagTxt"> {{image.country}} </span> </v-list-item-subtitle>
                        </v-list-item-content>
                    </v-col>
                    <v-col cols="2">
                        <v-rating
                            color="yellow darken-3"
                            background-color="yellow darken-3"
                            empty-icon="$ratingFull"
                            class="pb-7"
                            ></v-rating>
                    </v-col>
                       
                    </v-list-item>
                    
                </v-row>
                <v-row>
                    <v-col>
                        <p class="cardTxt">{{image.text}}</p>
                    </v-col>
                </v-row>
               
              </v-card>
              
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-row>
  </v-container>
</v-container>

</template>

<script>
export default {
    data:()=>({
        images:[
            {
                avatar:'asset 50.jpg', name:"Lee S.", country:"United States", flag:'asset 51.png',text:"Great day and experience with Boat as a true local guide"
            },
            {
                avatar:'asset 52.jpg', name:"mami m.", country:"JP Japan", flag:'asset 53.png',text:"Absolutely wonderful! Going on the trip with Piangduan was absolutely amazing,"
            },
            {
                avatar:'asset 54.jpg', name:"Joseph G.", country:"United Kingdom", flag:'asset 55.png',text:"Everything was above the expectations!"
            },
            {
                avatar:'asset 56.jpg', name:"Kate L.", country:"CA Canada", flag:'asset 57.png',text:"We had a great time with Kiki! He gave us lots of time to explore the temples - and the.."
            },
            {
                avatar:'asset 58.jpg', name:"Ilaria C.", country:"IT Italy", flag:'asset 59.png',text:"Great day and experience with Boat as a true local guide"
            },
            {
                avatar:'asset 60.jpg', name:"Joe H.", country:"US United States", flag:'asset 51.png',text:"Everything was above the expectations!"
            }
        ]
    })
}
</script>

<style>
  .v-rating .v-icon{
    padding: 0!important;
    font-size: 16px!important;
  }
  .cardTxt{
    padding: 0 21px!important;
    font-size: small;
    font-size: 14px!important;
    font-weight: 600!important;
    color: #4d4d5b!important;
    font-family: 'Open Sans'!important;
    margin: -15px 0;
} 
.TrvRevCrd{
  background-color: #244b521a!important;
  border-radius: 14px!important;
}
.userName{
  font-family: 'Open Sans'!important;
  font-weight: 600;
  color: #4d4d5b!important;
}
.flagTxt{
      font-weight: 600;
      font-family: 'Open Sans'!important;
    }
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
    .TrvRevCrd{
      width: 290px!important;
      height: 170px!important;
    }
    .flagTxt{
      font-size: 10px;
      font-weight: 400;
      font-family: 'Open Sans'!important;
    }
  }
</style>