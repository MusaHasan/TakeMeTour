<template>
<v-container fluid class="pa-0 BodyBGcolot">
  <v-container fluid class="childContainer">
      <v-row class="searchSec transparent" justify-md="center">
          <v-col class="searchCol" sm="6" xs="4" md="8" cols="8">
              
              <!-- <v-menu transition="slide-x-transition" offset-y >
                    <template v-slot:activator="{ on }">
                        <v-btn color="secondary" v-on="on" text small>
                            Button
                            <v-avatar size="28" class="pl-1">
                                <img
                                >
                            </v-avatar>
                            <v-icon right>mdi-chevron-down</v-icon>
                        </v-btn>
                    </template>
                    <v-list dense nav min-width="200">
                        <div v-if="! $route.path.includes('dashboard')">
                            <v-list-item class="text-left" dense v-for="item in nav_items" :key="item.title" :to="item.url">
                                <v-list-item-icon class="mr-3">
                                    <v-icon color="grey darken-2" class="body-1">{{ item.icon }}</v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>
                                    <v-list-item-title  class="caption grey--text text--darken-3">{{ item.title }}</v-list-item-title>
                                </v-list-item-content>
                            </v-list-item>
                            <v-divider></v-divider>
                        </div>
                        <v-list-item class="text-left">
                            <v-list-item-icon class="mr-3">
                                <v-icon color="grey darken-2" class="body-1"> mdi-exit-to-app </v-icon>
                            </v-list-item-icon>
                            <v-list-item-content>
                                <v-list-item-title class="caption grey--text text--darken-3"></v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list>
                </v-menu> -->

            <v-overflow-btn
            class="white shadow Search-btn"
            color="orange darken-3"
            prepend-icon="mdi-map-marker-outline"
            :items="dropdown_font"
            label="Where to go?"
            target="#dropdown-example"
            
            ></v-overflow-btn>

            <!-- <v-select
                v-model="selectedFruits"
                :items="fruits"
                label="Favorite Fruits"
                outlined 
                class="white"
            >
                <template v-slot:prepend-item>
                    <v-list-item
                    ripple
                    @click="toggle"
                    >
                    <v-list-item-action>
                        <v-icon :color="selectedFruits.length > 0 ? 'indigo darken-4' : ''">{{ icon }}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>Select All</v-list-item-title>
                    </v-list-item-content>
                    </v-list-item>
                    <v-divider class="mt-2"></v-divider>
                </template>
                <template v-slot:append-item>
                    <v-divider class="mb-2"></v-divider>
                    <v-list-item disabled>
                    <v-list-item-avatar color="grey lighten-3">
                        <v-icon>mdi-food-apple</v-icon>
                    </v-list-item-avatar>

                    <v-list-item-content v-if="likesAllFruit">
                        <v-list-item-title>Holy smokes, someone call the fruit police!</v-list-item-title>
                    </v-list-item-content>

                    <v-list-item-content v-else-if="likesSomeFruit">
                        <v-list-item-title>Fruit Count</v-list-item-title>
                        <v-list-item-subtitle>{{ selectedFruits.length }}</v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-content v-else>
                        <v-list-item-title>
                        How could you not like fruit?
                        </v-list-item-title>
                        <v-list-item-subtitle>
                        Go ahead, make a selection above!
                        </v-list-item-subtitle>
                    </v-list-item-content>
                    </v-list-item>
                </template>
                </v-select> -->
          </v-col>
          <v-col width="auto" class="buttonCol" sm="2" xs="2" cols="2">
            <v-btn max-width="133" max-height="48" height="48" class="searchBtn text-capitalize font-weight-bold subtitle-1" color="orange darken-3" dark>Explore</v-btn>
          </v-col>
      </v-row>
    
  </v-container>
</v-container>
</template>
<script>
  export default {

    data: () => ({
      dropdown_font: ['Arial', 'Calibri', 'Courier', 'Verdana','erert', 'erter', 'trtr', '434'],
      dropdown_icon: [
        { text: 'list', callback: () => console.log('list') },
        { text: 'favorite', callback: () => console.log('favorite') },
        { text: 'delete', callback: () => console.log('delete') },
        { text: 'list', callback: () => console.log('list') },
        { text: 'favorite', callback: () => console.log('favorite') },
        { text: 'delete', callback: () => console.log('delete') }
      ],
      dropdown_edit: [
        { text: '100%' },
        { text: '75%' },
        { text: '50%' },
        { text: '25%' },
        { text: '0%' },
      ],
    }),
  
    // data: () => ({
        //       fruits: [
        //         'Apples',
        //         'Apricots',
        //         'Avocado',
        //         'Bananas',
        //         'Blueberries',
        //         'Blackberries',
        //         'Boysenberries',
        //         'Bread fruit',
        //         'Cantaloupes (cantalope)',
        //         'Cherries',
        //         'Cranberries',
        //         'Cucumbers',
        //         'Currants',
        //         'Dates',
        //         'Eggplant',
        //         'Figs',
        //         'Grapes',
        //         'Grapefruit',
        //         'Guava',
        //         'Honeydew melons',
        //         'Huckleberries',
        //         'Kiwis',
        //         'Kumquat',
        //         'Lemons',
        //         'Limes',
        //         'Mangos',
        //         'Mulberries',
        //         'Muskmelon',
        //         'Nectarines',
        //         'Olives',
        //         'Oranges',
        //         'Papaya',
        //         'Peaches',
        //         'Pears',
        //         'Persimmon',
        //         'Pineapple',
        //         'Plums',
        //         'Pomegranate',
        //         'Raspberries',
        //         'Rose Apple',
        //         'Starfruit',
        //         'Strawberries',
        //         'Tangerines',
        //         'Tomatoes',
        //         'Watermelons',
        //         'Zucchini',
        //       ],
        //       selectedFruits: [],
        //     }),

        //     computed: {
        //       likesAllFruit () {
        //         return this.selectedFruits.length === this.fruits.length
        //       },
        //       likesSomeFruit () {
        //         return this.selectedFruits.length > 0 && !this.likesAllFruit
        //       },
        //       icon () {
        //         if (this.likesAllFruit) return 'mdi-close-box'
        //         if (this.likesSomeFruit) return 'mdi-minus-box'
        //         return 'mdi-checkbox-blank-outline'
        //       },
        //     },

        //     methods: {
        //       toggle () {
        //         this.$nextTick(() => {
        //           if (this.likesAllFruit) {
        //             this.selectedFruits = []
        //           } else {
        //             this.selectedFruits = this.fruits.slice()
        //           }
        //         })
        //       },
    //     },
  }
</script>
<style >
    .v-input__slot{
        min-height: 48px!important;
        padding: 0;
    }
    .searchSec{
            margin: 0 11%!important;
            position: relative;
            top: -50px;
            margin-left: 48px;
        }
    .v-text-field__details{
        margin-bottom: -21px!important;
    }
    .v-input__append-inner{
        margin-top: 0!important;
    }
    .Search-btn{
        box-shadow: -1px 0px 9px 1px rgba(148,148,148,1)!important;
        height: 48px!important;
        border: 1px solid rgb(238, 243, 245)!important;
        border-radius: 4px!important;
        transition: all 0.2s cubic-bezier(0.645, 0.045, 0.355, 1) 0s;  
    }
    .shadow{
        box-shadow: 0px 0px 5px 0px rgba(0,0,0,0.75)!important;
    }
    .v-overflow-btn .v-input__slot, .v-text-field.v-text-field--solo{
        box-shadow:transparent !important;
        border-style: none!important;
    }
    .v-overflow-btn.v-input--is-focused .v-input__slot, .v-overflow-btn.v-select--is-menu-active .v-input__slot {
    border-color: transparent !important;
    box-shadow: 0 1px 6px 0 rgba(255, 255, 255, 0.28)!important;
}
    .Search-btn .mdi:before{
        padding-left: 25px;
        color: #EF6C00;
    }
    .searchCol{
        background-color: #F8FBFB;
        border-radius: 10px 0 0 0;
        margin-left: 36px;
        margin-right: 0; 
    } 
    .searchCol .v-text-field {
        padding-top: 0px;
        padding-right: 20px;
        margin-top: 4px;
    }
    .buttonCol{
        background-color: #F8FBFB;
        border-radius: 0 10px 0 0;
        padding: 14px 4px!important;
    }  
    .searchBtn{
        padding: 0 50px!important;
    } 
    @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .searchSec{
        position: relative;
        top: -34px;
        margin-left: 0 !important;
        width: auto;
        margin-right:-13% !important;
        }
        .searchCol{
        background-color: #f8fbfb00;
        border-radius: 0;
        margin-left: 0px;
       
        } 
        .buttonCol{
            background-color: #f8fbfb00;
            border-radius: 0;
            margin: 0px ;
            padding: 19px 4px!important;
        } 
        .searchBtn{
            padding: 0px 3px!important;
            font-size: 12px!important;
            margin: -3px;
        } 
        
    }
    @media only screen
    and (min-device-width : 768px)
    and (max-device-width : 1224px) {
        .searchSec{
            position: relative;
            top: -34px;
            margin-right: 60px!important;
            margin-left: 40px!important;
            left: 70px;
        }
        .searchCol{
        background-color: #f0f8ff00;
        border-radius: 0;
        margin-left: 0px;
        margin-right: 0;
        } 
        .buttonCol{
            background-color: #f0f8ff00;
            border-radius: 0;
        }
        .searchBtn{
            padding:0 28px;
        }  
    }
    @media (min-width: 1904px){
    .searchCol{
        background-color: #F8FBFB;
        border-radius: 10px 0 0 0;
        margin-left: 36px;
        margin-right: 0;
    } 
    .buttonCol{
        background-color: #F8FBFB;
        border-radius: 0 10px 0 0;
        padding: 14px 4px!important;
    }  
    }
</style>