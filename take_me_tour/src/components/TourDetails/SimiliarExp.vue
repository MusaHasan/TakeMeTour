<template>
<v-container fluid class="pa-0 BodyBGcolot">
    <v-container class="childContainer">
      <v-row >
            <h3>Tour Available Tomorrow</h3>
            
            <v-col md="3" lg="3" xl="3" cols="12" class="ml-2 mb-2" 
                v-for="(image,i) in images" :key="i">
                <v-card
                    class="mx-auto white TurAvCrd"
                    max-width="min-content"
                    max-height="355"
                >
                    <v-img
                    class="white--text align-end"
                    height="206px"
                    width="270px"
                    :src="require(`../../assets/images/${image.name}`)"
                    >
                    </v-img>

                    <v-card-subtitle class="tagTxt">Number 10</v-card-subtitle>

                    <v-card-text class="text--primary">
                    <div>Whitehaven Beach</div>

                    <div>Whitsunday Island, Whitsunday Islands</div>
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
  .TurAvCrd{
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
  @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
      .TurAvCrd{
        width: 273px!important;
        height: 209px!important;
      }
    }

</style>
