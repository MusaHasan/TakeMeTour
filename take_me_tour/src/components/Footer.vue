<template>
<v-container fluid class="pa-0 FootbgColor">
  <v-container>
      <v-row>
          <v-col cols="3" class="px-12">
              <h4>Currency</h4>
              <v-row>
                    <v-overflow-btn
                    class="my-2"
                    :items="dropdown_icon"
                    label="Segmented Btn"
                    segmented
                    target="#dropdown-example"
                    ></v-overflow-btn>
              </v-row>
              <h4>Country</h4>
              <v-row>
                    <v-overflow-btn
                    class="my-2"
                    :items="dropdown_icon"
                    label="Segmented Btn"
                    segmented
                    target="#dropdown-example"
                    ></v-overflow-btn>
              </v-row>
              <h4>Follow us on</h4>
              <v-row>
                <v-icon class="socialIc pa-1" v-for="(icon,i) in icons" :key="i">{{icon.name}}</v-icon>  
              </v-row>
          </v-col>

          <v-col cols="3">
              <h4>About TakeMeTour</h4>
              <v-row>
                    <v-list-item>
                        <v-list-item-content>
                            <v-list-item-subtitle class="socialIc" v-for="(item,i) in AbTMT" :key="i" >{{item.txt}}</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
              </v-row>
              <h4>Our Projects</h4>
              <v-row>
                  <v-list-item>
                    <v-list-item-content>
                        <v-list-item-subtitle class="socialIc" v-for="(item,i) in OuProj" :key="i" >{{item.txt}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item> 
              </v-row>
          </v-col>
          <v-col cols="3">
              <h4>Top Destinations</h4>
              <v-row>
                  <v-list-item>
                    <v-list-item-content >
                        <v-list-item-subtitle class="socialIc" v-for="(item,i) in TopDes" :key="i" >{{item.txt}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item> 
              </v-row>
          </v-col>
          <v-col cols="3">
              <h4>Top Activities</h4>
              <v-row>
                  <v-list-item>
                    <v-list-item-content >
                        <v-list-item-subtitle class="socialIc" v-for="(item,i) in TopAct" :key="i" >{{item.txt}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item> 
              </v-row>
          </v-col>
      </v-row>
  </v-container>
  </v-container>
</template>

<script>
export default {
    data:()=>({
        icons:[
            {name: "mdi-facebook"}, {name: "mdi-instagram"}, {name: "mdi-pinterest"}, {name: "mdi-twitter"}
        ],
        AbTMT: [
            {txt:'About Us'},
            {txt:'Affiliate Program'},
            {txt:'Influencer Program'},
            {txt:'Blog'},
            {txt:'Careers'},
            {txt:'Help Center'},
            {txt:'Privacy Policy'},
            {txt:'Sitemap'},
            {txt:'T&C'},
            {txt:'Travel e-book'},
            {txt:'Trust & Safety'}
        ],
        OuProj: [
            {txt:'Amazing Thailand'},
            {txt:'Biennale Krabi 2018'},
            {txt:'Local Table'},
            {txt:'Thanks A Million'},
        ],
        TopDes: [
            {txt:'Ayutthaya Tours'},
            {txt:'Bangkok Tours'},
            {txt:'Tours from Bangkok'},
            {txt:'Chiang Mai Tours'},
            {txt:'Chiang Rai Tours'},
            {txt:'Tours from Chiang Mai'},
            {txt:'Hat Yai Tours'},
            {txt:'Hua Hin Tours'},
            {txt:'Kanchanaburi Tours'},
            {txt:'Khao Yai Tours'},
            {txt:'Koh Samui Tours'},
            {txt:'Krabi Tours'},
            {txt:'Pattaya Tours'},
            {txt:'Phuket Tours'},
            {txt:'Tours from Phuket'},
            {txt:'Central Thailand Tours'},
            {txt:'Eastern Thailand Tours'},
            {txt:'Northeastern Thailand Tours'},
            {txt:'Northern Thailand Tours'},
            {txt:'Southern Thailand Tours'},
            ],
        TopAct: [
            {txt:'City Tour'},
            {txt:'Natural'},
            {txt:'Floating Market'},
            {txt:'Cooking Class'},
            {txt:'Beach'},
            {txt:'Cycling'},
            {txt:'Boating'},
            {txt:'Street Food'},
            {txt:'Property Tours'},
        ],
        dropdown_font: ['Arial', 'Calibri', 'Courier', 'Verdana'],
        dropdown_icon: [
            { text: 'list', callback: () => console.log('list') },
            { text: 'favorite', callback: () => console.log('favorite') },
            { text: 'delete', callback: () => console.log('delete') },
        ],
        dropdown_edit: [
            { text: '100%' },
            { text: '75%' },
            { text: '50%' },
            { text: '25%' },
            { text: '0%' },
        ],
    })
}
</script>

<style>
    .socialIc{
        color: #2F424C!important;
    }
    .FootbgColor{
        background-color: #F0F5F7;
    }
</style>