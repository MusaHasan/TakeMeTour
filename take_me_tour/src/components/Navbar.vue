<template>
  <div>
    <v-app-bar
        
        elevation="0"
        fixed
        max-height="56"
        color="white"
        dark
    >
    
        <v-img class="pl-1" max-width="145" max-height="22" src="../assets/images/asset 0.png"></v-img>
        <v-spacer class="d-md-none"></v-spacer>
        <v-btn class="mx-3 body-2 font-weight-light white--text text-capitalize " max-width="109" max-height="32" tile style="background-color:#21D366">Contact Us</v-btn>
        <v-spacer></v-spacer>
        <v-list class="d-md-flex d-lg-flex hidden-sm-and-down transparent ">

            <v-list-item> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-title class="grey--text"  v-on="on" >Where to go?
                    <v-icon class="grey--text">mdi-chevron-down</v-icon>
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

            <v-list-item> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-title class="grey--text"  v-on="on" >Travel Products
                    <v-icon class="grey--text">mdi-chevron-down</v-icon>
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

            <div class="my-2 mx-2">
              <v-btn text large color="orange darken-3" > <v-icon class="grey--text">mdi-cash-usd-outline</v-icon> <span class="grey--text">Deals</span> </v-btn>
            </div>

            <div class="my-2 mx-2">
              <v-btn outlined large color="orange darken-3">log In</v-btn>
            </div>

            <div class="my-2 mx-2">
              <v-btn large color="orange darken-3">Sign Up</v-btn>
            </div>

            <v-list-item> 
              <v-menu offset-y>
                <template v-slot:activator="{ on }">
                  <v-list-item-title class="grey--text"  v-on="on" >USD
                    <v-icon class="grey--text">mdi-chevron-down</v-icon>
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
        <div class="text-center hidden-lg-and-up">
            <template>
                <v-app-bar-nav-icon color="orange darken-3" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            </template>
          <v-navigation-drawer
            v-model="drawer"
            absolute
            temporary
            class="white"
            height="660"
            right
          >

            <v-divider></v-divider>
          </v-navigation-drawer>
      </div>
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
</style>