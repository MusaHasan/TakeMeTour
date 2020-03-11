<template>
<v-container fluid class="pa-0 FootbgColor">
  <v-container class="childContainer">
      <v-row>
          <v-col md="3" lg="3" xl="3" cols="12" class="BtnDv">
              <h3 class="BtnTtl" >Currency</h3>
              <v-row>
                    <div class="text-center">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on }">
                                <v-hover v-slot:default="{ hover }">
                                    <v-btn
                                    class="footerBtn active mb-6"
                                    height="48"
                                    width="206"
                                    :ripple="false"
                                    light
                                    v-on="on"
                                    @click="isActive1=!isActive1"
                                    :elevation="hover ? 12 : 0"
                                    :class="{ 'on-hover': hover, activeBtn1 : isActive1 }"
                                    >
                                        <span class="mr-12">US Dollar</span><v-icon color="orange darken-4">mdi-chevron-down</v-icon>
                                    </v-btn>
                                </v-hover>
                            </template>
                            <v-list>
                                <v-list-item
                                v-for="(item, index) in items"
                                :key="index"
                                >
                                <v-list-item-title>{{ item.title }}</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </div>
              </v-row>
              <h3 class="BtnTtl">Country</h3>
              <v-row>
                    <div class="text-center">
                        <v-menu offset-y>
                            <template v-slot:activator="{ on }">
                                <v-hover v-slot:default="{ hover }">
                                    <v-btn
                                    class="footerBtn mb-6"
                                    height="48"
                                    width="206"
                                    :ripple="false"
                                    @click="isActive2=!isActive2"
                                    v-on="on"
                                    :elevation="hover ? 12 : 0"
                                    :class="{ 'on-hover': hover, activeBtn2 : isActive2 }"
                                    >
                                        <span class="mr-12 ">United States</span><v-icon color="orange darken-4">mdi-chevron-down</v-icon>
                                    </v-btn>
                                </v-hover>
                            </template>
                            <v-list>
                                <v-list-item
                                v-for="(item, index) in items"
                                :key="index"
                                >
                                <v-list-item-title>{{ item.title }}</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </div>
              </v-row>
              <h3 class="BtnTtl">Follow us on</h3>
              <v-row>
                <v-icon class="socialIc pa-1" v-for="(icon,i) in icons" :key="i">{{icon.name}}</v-icon>  
              </v-row>
          </v-col>

          <v-col md="3" lg="3" xl="3" cols="12">
              <h3 class="listTtl">About TakeMeTour</h3>
              <v-row>
                    <v-list-item>
                        <v-list-item-content>
                            <v-list-item-subtitle class="socialIc mb-1" v-for="(item,i) in AbTMT" :key="i" >{{item.txt}}</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
              </v-row>
              <h3 class="listTtl">Our Projects</h3>
              <v-row>
                  <v-list-item>
                    <v-list-item-content>
                        <v-list-item-subtitle class="socialIc mb-1" v-for="(item,i) in OuProj" :key="i" >{{item.txt}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item> 
              </v-row>
          </v-col>
          <v-col md="3" lg="3" xl="3" cols="12">
              <h3 class="listTtl">Top Destinations</h3>
              <v-row>
                  <v-list-item>
                    <v-list-item-content >
                        <v-list-item-subtitle class="socialIc mb-1" v-for="(item,i) in TopDes" :key="i" >{{item.txt}}</v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item> 
              </v-row>
          </v-col>
          <v-col md="3" lg="3" xl="3" cols="12">
              <h3 class="listTtl">Top Activities</h3>
              <v-row>
                  <v-list-item>
                    <v-list-item-content >
                        <v-list-item-subtitle class="socialIc mb-1" v-for="(item,i) in TopAct" :key="i" >{{item.txt}}</v-list-item-subtitle>
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
        isActive1: false,
        isActive2: false,
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
        items: [
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me 2' },
        ],
    })
}
</script>

<style>
    .socialIc{
        color: #2F424C!important;
        transition: opacity .4s ease-in-out!important;
    }
    .socialIc:not(.on-hover) {
    opacity: 0.6!important;
    }
    .FootbgColor{
        background-color: #F0F5F7;
    }
    .BtnDv{padding: 4px 48px;}
    .footerBtn {
        background-color: white!important;
    }
    .v-input__control{
        height: 34px!important;
    }
    .v-autocomplete.v-input{
        border-style: hidden!important;
    }
    .activeBtn1,.activeBtn2{
         border: 1px solid #ff7b00!important;
         background-color: white!important;
    }
    .BtnTtl{
        margin: 8px -11px;
    }
    .listTtl{
         margin: 6px 2px;
    }
    @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px){
        .BtnDv{
            padding: 4px 25px;
        }
        
    }
    
</style>