<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container class="childContainer">
      <v-row >
        <h2 class="TitelTxt">Travel Products</h2>
        <v-sheet
          class="mx-auto transparent"
          elevation="0"
          max-width="100%"
        >
          <v-slide-group
            class="pa-0"
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
              class="ml-2"
            >
              
              <v-card
                class="ma-1 TeProCrd"
                height="150"
                width="178"
                :ripple="false"
              >
                <v-img
                class="white--text mt-6 mx-auto"
                height="62"
                width="70"
                :src="require(`../../assets/images/${image.name}`)"
                >
                </v-img>
                <p class="text-center body-2">4G Sim Card</p>
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
                name:'asset 32.svg', label:'asset 7.png'
            },
            {
                name:'asset 33.svg', label:'asset 8.png'
            },
            {
                name:'asset 34.svg', label:'asset 9.png'
            },
            {
                name:'asset 35.svg', label:'asset 10.png'
            },
            {
                name:'asset 36.svg', label:'asset 11.png'
            },
            {
                name:'asset 37.svg', label:'asset 12.png'
            },
            {
                name:'asset 38.svg', label:'asset 12.png'
            },
            {
                name:'asset 39.svg', label:'asset 12.png'
            }
        ]
    })
}
</script>

<style>
.TeProCrd{
  background-color: #FFFFFF!important;
  cursor: pointer;
  border-radius: 12px!important;
  box-shadow: rgba(36, 75, 82, 0.1) 0px 3px 5px 0px;
}
@media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
    .TeProCrd{
      width: 143px!important;
    }
  }
</style>