<template>
  <div>
    <v-app-bar
        
        elevation="0"
        fixed
        max-height="56"
        color="white"
        dark
    >
    
        <v-img class="pl-1 navbarTitelImg" max-width="145" max-height="22" src="../assets/images/asset 0.png"></v-img>
        <v-spacer class="d-md-none"></v-spacer>
        <v-btn class="mx-1 mx-md-3 mx-lg-3 mx-xl-3 navBtnContact body-2 font-weight-light white--text text-capitalize " max-width="109" max-height="32" tile style="background-color:#21D366">Contact Us</v-btn>
        <v-list-item style="max-width: fit-content;" class="hidden-lg-and-up px-0"> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-title style="font-size:12px!important" class="black--text"  v-on="on" >USD
                    <v-icon size="18" class="black--text mb-2 font-weight-thin">mdi-chevron-down</v-icon>
                  </v-list-item-title>
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
          </v-list-item>
        <v-spacer class="hidden-sm-and-down"></v-spacer>
        <v-list class="d-md-flex d-lg-flex hidden-sm-and-down transparent ">

            <v-list-item class="px-0"> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-subtitle class="black--text"  v-on="on" >Where to go?
                    <v-icon class="black--text font-weight-thin">mdi-chevron-down</v-icon>
                  </v-list-item-subtitle>
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
            </v-list-item>

            <v-list-item class="px-0"> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-subtitle class="black--text"  v-on="on" >Travel Products
                    <v-icon class="black--text .font-weight-thin">mdi-chevron-down</v-icon>
                  </v-list-item-subtitle>
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
            </v-list-item>

            <div class="my-2 mx-2">
              <v-btn class="px-1" text large color="orange darken-3" > <v-img class="mx-2" max-width="16" max-height="17" src="../assets/Tourimage/asset 95.jpg"></v-img> <span class="black--text">Deals</span> </v-btn>
            </div>

            <div class="my-2 mx-2">
              <v-btn class="px-0" height= "38" outlined large color="orange darken-3">log In</v-btn>
            </div>

            <div class="my-2 mx-2">
              <v-btn height= "38" large color="orange darken-3">Sign Up</v-btn>
            </div>

            <v-list-item> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-title class="black--text"  v-on="on" >USD
                    <v-icon class="black--text font-weight-thin">mdi-chevron-down</v-icon>
                  </v-list-item-title>
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
          </v-list-item>
        </v-list>
                
        <div class="text-center sideBarBg hidden-lg-and-up">
            <template>
                <v-app-bar-nav-icon color="orange darken-3" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            </template>
          <v-navigation-drawer
            v-model="drawer"
            absolute
            temporary 
            class="white sideBar"
            height="660"
            width="241"
            right
          >
            <v-row>
              <v-col>
                <div class="my-2 mx-2">
                  <v-btn class="mt-1" height= "38" max-width="174" width="175" large color="orange darken-3">Sign Up</v-btn>
                </div>

                <div class="my-2 mx-2">
                  <v-btn height= "38" max-width="174" width="175" outlined large color="orange darken-3">log In</v-btn>
                </div>

                <div class=" mb-2 mt-4 mx-8" style="border-bottom: 1px solid #c8c8c8;"></div><!--Light HR line border-->

                <div class="mt-0 mb-2 ml-0 mr-2">
                  <v-btn text max-width="174" width="175" class="ml-8 pl-3 d-flex justify-start" large color="orange darken-3" > <v-img class="mr-2" max-width="16" max-height="17" src="../assets/Tourimage/asset 95.jpg"></v-img> <span class="text-left" style="color: rgb(0, 0, 0) !important; font-weight: 500;">Deals</span> </v-btn>
                </div>
                
                <v-row class="mx-10">
                  <v-icon color="rgb(66, 94, 108)" class="pa-2" v-for="(icon,i) in icons" :key="i">{{icon.name}}</v-icon>  
                </v-row>

                <v-list-item> 
                  <v-menu offset-y>
                    <template v-slot:activator="{ on }">
                      <v-list-item-subtitle style="color: rgb(0, 0, 0) !important; font-weight: 500; margin-left: 20px;"  v-on="on" >Where to go?
                        <v-icon style="margin-left:36px" class="grey--text">mdi-chevron-down</v-icon>
                      </v-list-item-subtitle>
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
                </v-list-item>

                <v-list-item> 
                  <v-menu offset-y>
                    <template v-slot:activator="{ on }">
                      <v-list-item-subtitle style="color: rgb(0, 0, 0) !important; font-weight: 500; margin-left: 20px;"  v-on="on" >Travel Products
                        <v-icon style="margin-left:24px" class="grey--text">mdi-chevron-down</v-icon>
                      </v-list-item-subtitle>
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
                </v-list-item>

              </v-col>
              
            </v-row>
            <v-divider>
            </v-divider>
          </v-navigation-drawer>
      </div> <!--Mini Side bar-->
<!-- 
      <v-img class="pl-1" max-width="145" max-height="22" src="../assets/images/asset 0.png"></v-img>
      <v-spacer class="d-md-none"></v-spacer>
      <v-btn class="mx-3 body-2 font-weight-light white--text text-capitalize " max-width="109" max-height="32" tile style="background-color:#21D366">Contact Us</v-btn> -->
        
    </v-app-bar>
  </div>
</template>
<script>
  export default {
    data: () => ({
      drawer: null,
      items: [
        { title: 'Home', icon: 'dashboard' },
        { title: 'About', icon: 'question_answer' },
      ],
      icons:[
        {name: "mdi-facebook"}, {name: "mdi-instagram"}, {name: "mdi-pinterest"}, {name: "mdi-twitter"}
      ],
    }),
  }
</script>
<style>
    .v-toolbar__content{
        height: 56px!important; 
    }
    .v-responsive__sizer{
        height: 22px;
    }
    .v-overlay__scrim{
      height: 660px!important;
      width: 10px;
    }
    .sideBar{
      margin-top: 56px!important;
    }
    .sideBarBg{
      margin-left: -6px;
    }
    .sideBarBg .v-overlay__scrim{
      margin: 56px 0;
    } 
    .sideBarBg .v-navigation-drawer--is-mobile{
      box-shadow: unset!important;
    }
    @media only screen
    and (min-device-width : 300px)
    and (max-device-width : 767px){
    .navBtnContact{
      max-width: 83px!important;
      margin-top: -5px;
    }
    .navbarTitelImg .v-image__image{
       width: 100%!important;
    }

    }
    @media only screen and (max-device-width: 320px)
    {
      .sideBarBg{
      margin-left: -17px;
    }
    .navBtnContact{
      margin:0 0 !important;
    }
    }
</style>