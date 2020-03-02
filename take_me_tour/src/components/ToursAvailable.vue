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
            class="pa-2"
          >
            <v-slide-item
              v-for="(image,i) in images"
              :key="i"
            >
                <v-card
                    class="mx-auto"
                    max-width="100%"
                    max-height="355"
                >
                    <v-img
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    :src="require(`../assets/images/${image.name}`)"
                    >
                    </v-img>

                    <v-card-subtitle class="pb-0">Number 10</v-card-subtitle>

                    <v-card-text class="text--primary">
                    <div>Whitehaven Beach</div>

                    <div>Whitsunday Island, Whitsunday Islands</div>
                    </v-card-text>

                </v-card>
        
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </v-row>
    </v-container>
</template>

<script>
// @ is an alias to /src


export default {
    data:()=>({
        images:[
            {
                name:'asset 13.png', label:'asset 7.png'
            },
            {
                name:'asset 15.png', label:'asset 8.png'
            },
            {
                name:'asset 16.jpg', label:'asset 9.png'
            },
            {
                name:'asset 17.png', label:'asset 10.png'
            },
            {
                name:'asset 21.jpg', label:'asset 11.png'
            },
            {
                name:'asset 22.jpg', label:'asset 12.png'
            },
            {
                name:'asset 25.png', label:'asset 12.png'
            },
            {
                name:'asset 27.png', label:'asset 12.png'
            },
            {
                name:'asset 27.png', label:'asset 12.png'
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
