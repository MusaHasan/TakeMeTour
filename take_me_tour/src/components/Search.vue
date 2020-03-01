<template>
  <v-container fluid>
      <v-row class="ml-12  searchSec transparent" justify-md="center">
          <v-col class="searchCol" sm="6" xs="4"  md="8" cols="8">
              
            <v-overflow-btn
            class="white"
            color="orange darken-3"
            :items="dropdown_font"
            label="Overflow Btn"
            target="#dropdown-example"
            solo
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
            <v-btn max-width="150" max-height="48" height="48" class="searchBtn" color="orange darken-3" dark>Explore</v-btn>
          </v-col>
      </v-row>
    
  </v-container>
</template>
<script>
  export default {

    data: () => ({
      dropdown_font: ['Arial', 'Calibri', 'Courier', 'Verdana','Arial', 'Calibri', 'Courier', 'Verdana'],
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
        }
    .v-text-field__details{
        margin-bottom: -21px!important;
    }
    .v-input__append-inner{
        margin-top: 0!important;
    }
    .searchCol{
        background-color: #F8FBFB;
        border-radius: 10px 0 0 0;
    } 
    .buttonCol{
        background-color: #F8FBFB;
        border-radius: 0 10px 0 0;
        padding: 14px 20px!important;
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
        width: 96%;
        margin: 0!important;
        }
        .searchCol{
        background-color: #f8fbfb00;
        border-radius: 0;
        } 
        .buttonCol{
            background-color: #f8fbfb00;
            border-radius: 0;
        } 
        .searchBtn{
            padding: 0px 3px!important;
            font-size: 12px!important;
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
        } 
        .buttonCol{
            background-color: #f0f8ff00;
            border-radius: 0;
        }
        .searchBtn{
            padding:0 28px;
        }  
    }
</style>