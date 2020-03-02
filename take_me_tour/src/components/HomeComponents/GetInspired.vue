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
              <v-hover
                    v-slot:default="{ hover }"
                    open-delay="200"
                >
              <v-card
                :color="active ? 'primary' : 'grey lighten-1'"
                class="ma-1"
                height="320"
                width="218"
                @click="toggle"
              >
                <v-img
                    class="white--text img align-end"
                    :height="hover ? '110%':'100%'"
                    :src="require(`../../assets/images/${image.name}`)"
                >
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
</style>
