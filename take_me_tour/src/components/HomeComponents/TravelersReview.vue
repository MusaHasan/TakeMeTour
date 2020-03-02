<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container>
      <v-row >
          <h2 class="mx-10">Get Inspired</h2>
        <v-sheet
          class="mx-auto"
          elevation="0"
          max-width="100%"
        >
          <v-slide-group
            class="pa-0"
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
              v-slot:default="{ active, toggle }"
            >
              <v-card
                :color="active ? 'primary' : 'grey lighten-1'"
                class="ma-1"
                height="170"
                width="369"
                @click="toggle"
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
                    <v-col cols="6">
                        <v-list-item-content>
                            <v-list-item-title>{{image.name}}</v-list-item-title>
                             <v-list-item-title> 
                                    <v-img
                                        class="white--text d-inline-block"
                                        height="20"
                                        width="30"
                                        :src="require(`../../assets/images/${image.flag}`)"
                                    >
                                    </v-img> {{image.country}}</v-list-item-title>
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
                        <p class="cardTxt">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                         Consequatur maxime eligendi iure ipsa cum! Reiciendis quam molestiae voluptas.</p>
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
                avatar:'asset 50.jpg', name:"Lee S.", country:"United States", flag:'asset 51.png'
            },
            {
                avatar:'asset 52.jpg', name:"mami m.", country:"JP Japan", flag:'asset 53.png'
            },
            {
                avatar:'asset 54.jpg', name:"Joseph G.", country:"GB United Kingdom", flag:'asset 55.png'
            },
            {
                avatar:'asset 56.jpg', name:"Kate L.", country:"CA Canada", flag:'asset 57.png'
            },
            {
                avatar:'asset 58.jpg', name:"Ilaria C.", country:"IT Italy", flag:'asset 59.png'
            },
            {
                avatar:'asset 60.jpg', name:"Joe H.", country:"US United States", flag:'asset 51.png'
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
        padding: 0 17px!important;
        font-size: small;
}
</style>