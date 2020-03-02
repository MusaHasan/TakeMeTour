<template>
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
                :color="active ? 'primary' : 'white lighten-1'"
                class="ma-1"
                height="150"
                width="178"
                @click="toggle"
              >
                <v-img
                class="white--text mt-6 mx-auto"
                height="62"
                width="70"
                :src="require(`../assets/images/${image.name}`)"
                >
                </v-img>
                <p class="text-center">4g sim card</p>
              </v-card>
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-row>
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

</style>