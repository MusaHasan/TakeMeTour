<template>
<v-container fluid class="pa-0 BodyBGcolot">
    <v-container class="childContainer pt-0">
      <v-row >
          <h2 class="TitelTxt TitleGet mb-4">Get Inspired</h2>
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
              v-slot:default="{ active, toggle }"
              class="ml-2 transparent"
            >
              <v-hover
                  v-slot:default="{ hover }"
                  open-delay="200"
                >
              <v-card
                :color="active ? 'primary' : 'grey lighten-1'"
                class="ma-1 imgCrd"
                height="320"
                width="218"
                :ripple="false"
                @click="toggle"
                router to="/about"
              >
                <v-img
                  class="white--text img align-end"
                  :height="hover ? '110%':'100%'"
                  :src="require(`../../assets/images/${image.name}`)"
                > 
                  <div class="fill-height bottom-gradient">
                    <v-row
                    class="fill-height"
                    align="center"
                    justify="center"
                    >
                    
                        <v-img
                            class="white--text align-end hoverIf"
                            height="100%"
                            :src="require(`../../assets/images/${image.label}`)"
                        >
                        </v-img>
                    </v-row>
                  </div>
                </v-img>
              </v-card>
              </v-hover>
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
                name:'asset 65.png', label:'asset 7.png'
            },
            {
                name:'asset 66.png', label:'asset 8.png'
            },
            {
                name:'asset 67.png', label:'asset 9.png'
            },
            {
                name:'asset 68.png', label:'asset 10.png'
            },
            {
                name:'asset 69.png', label:'asset 11.png'
            },
            {
                name:'asset 70.png', label:'asset 12.png'
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
  .GetSld{
    padding: 0;
  }
  .TitleGet{
    margin: -2px 35px!important;
  }
  
  @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
    .imgCrd{
      width: 148px!important;
      height: 258px!important;
      cursor: pointer;

    }
  }
</style>
