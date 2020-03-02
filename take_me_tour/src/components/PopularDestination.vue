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
                :color="active ? 'primary' : 'grey lighten-1'"
                class="ma-1"
                height="216"
                width="216"
                @click="toggle"
              >
                <v-img
                    class="white--text img align-end"
                    height="100%"
                    :src="require(`../assets/images/${image.name}`)"
                >
                    
                </v-img>
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
                name:'asset 42.jpeg', label:'asset 7.png'
            },
            {
                name:'asset 43.jpeg', label:'asset 8.png'
            },
            {
                name:'asset 44.jpeg', label:'asset 9.png'
            },
            {
                name:'asset 45.jpeg', label:'asset 10.png'
            },
            {
                name:'asset 46.jpeg', label:'asset 11.png'
            },
            {
                name:'asset 47.jpeg', label:'asset 12.png'
            },
            {
                name:'asset 48.jpeg', label:'asset 12.png'
            },
            {
                name:'asset 49.jpeg', label:'asset 12.png'
            }
        ]
    })
}
</script>

<style>

</style>