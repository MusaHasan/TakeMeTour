<template>
  <v-container>
      
        <v-row>
            <h3>Reviews (50)</h3> 
            <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating> 4.7
        </v-row>
        <v-row>
            <p>Friendliness</p> 
            <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating> 4.8
        </v-row> <!--Review text <loop>-->

        <v-row>
            <v-col>
                <div class="text-center">
                    <v-menu offset-y>
                    <template v-slot:activator="{ on }">
                        <v-hover v-slot:default="{ hover }">
                            <v-btn
                            class="active socialIc mb-6"
                            height="48"
                            width="206"
                            :ripple="false"
                            light
                            v-on="on"
                            @click="isActive1=!isActive1"
                            :elevation="hover ? 12 : 2"
                            :class="{ 'on-hover': hover, activeBtn1 : isActive1 }"
                            >
                                <span class="mr-12">Dropdown</span><v-icon color="orange darken-4">mdi-chevron-down</v-icon>
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
            </v-col>
            <v-col>
                <div class="text-center">
                    <v-menu offset-y>
                    <template v-slot:activator="{ on }">
                        <v-hover v-slot:default="{ hover }">
                            <v-btn
                            class="active socialIc mb-6"
                            height="48"
                            width="206"
                            :ripple="false"
                            light
                            v-on="on"
                            @click="isActive1=!isActive1"
                            :elevation="hover ? 12 : 2"
                            :class="{ 'on-hover': hover, activeBtn1 : isActive1 }"
                            >
                                <span class="mr-12">Dropdown</span><v-icon color="orange darken-4">mdi-chevron-down</v-icon>
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
            </v-col>
        </v-row> <!--Review Buttons-->
        <v-row>
            <v-col cols="2" v-for="(image,i) in images"
                :key="i">
                <v-card
                    class="ma-1 PopDesCrd"
                    height="216"
                    width="216"
                    :ripple="false"
                >
                    <v-img
                        class="white--text img align-end"
                        height="100%"
                        :src="require(`../../../assets/images/${image.name}`)"
                    >                    
                    </v-img>
                </v-card>
            </v-col> <!--Review images <loop 4 times>-->
            <v-col cols="1">
                <v-card
                    class="ma-1 PopDesCrd"
                    height="216"
                    width="216"
                    :ripple="false"
                >
                    <v-icon class="white--text img align-end"
                        height="100%"
                    >mdi-dots-horizontal</v-icon>
                </v-card>
            </v-col><!--images icon card-->
        </v-row><!--Review Images-->
        <v-row>
            <v-col md="8" lg="8" xl="8" cols="12"><!--title txt-->
                <h3>Street Food Tour in Bangkok Chinatown</h3>
                    <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating> 4.8
            </v-col>
            <v-col md="4" lg="4" xl="4" cols="12">
                    <v-row>
                        <v-list-item class="grow">
                            <v-col cols="2"> 
                                <v-list-item-avatar color="grey darken-3">
                                    <v-img
                                        class="elevation-6"
                                        src="../../../assets/Tourimage/asset 64.jpeg"
                                    ></v-img>
                                </v-list-item-avatar>
                            </v-col>
                            <v-col cols="6">
                                <v-list-item-content>
                                    <v-list-item-title>Hannah S.</v-list-item-title>
                                    <v-list-item-title>
                                        <p>February 19, 2020 </p> 
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-col>
                            <v-col cols="2">
                            </v-col>
                        
                        </v-list-item>
                        
                    </v-row>
            </v-col><!--user image & name-->
        </v-row> <!--Review Title reating F-iconImg-->
        <hr>
        <v-row>
            <v-col cols="12">
                <p>Eddie was very friendly, kind & knowledgeable of the Chinatown neighborhood. Being a native of 
                    Bangkok, he took me to some local favorite eateries that were very savory. It was great 
                    to have a local navigate me through this very exciting but busy area.
                        At the end we had a refreshing traditional Thai dessert :) It was an enjoyable experience.
                </p>
                <v-row>
                    <v-col cols="2" v-for="(image,i) in images"
                    :key="i">
                        <v-card
                            class="ma-1 PopDesCrd"
                            height="216"
                            width="216"
                            :ripple="false"
                        >
                            <v-img
                                class="white--text img align-end"
                                height="100%"
                                :src="require(`../../../assets/images/${image.name}`)"
                            >                    
                            </v-img>
                        </v-card>
                    </v-col> <!--Review images <loop 3 time>-->
                </v-row><!--Review Images-->
                <p>
                    Helpful? <v-icon style="border-right: 1px solid gray;">mdi-thumb-up-outline</v-icon> <v-icon>mdi-thumb-down-outline</v-icon>
                </p>
            </v-col>
        </v-row><!--Review text like dislike icon-->
        <hr>
        <v-row>
            <v-col md="8" lg="8" xl="8" cols="12"><!--title txt-->
                <h3>Street Food Tour in Bangkok Chinatown</h3>
                    <v-rating
                color="yellow darken-3"
                background-color="yellow darken-3"
                empty-icon="$ratingFull"
                class="py-3"
                ></v-rating> 4.8
            </v-col>
            <v-col md="4" lg="4" xl="4" cols="12">
                    <v-row>
                        <v-list-item class="grow">
                            <v-col cols="2"> 
                                <v-list-item-avatar color="grey darken-3">
                                    <v-img
                                        class="elevation-6"
                                        src="../../../assets/Tourimage/asset 64.jpeg"
                                    ></v-img>
                                </v-list-item-avatar>
                            </v-col>
                            <v-col cols="6">
                                <v-list-item-content>
                                    <v-list-item-title>Hannah S.</v-list-item-title>
                                    <v-list-item-title>
                                        <p>February 19, 2020 </p> 
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-col>
                            <v-col cols="2">
                            </v-col>
                        
                        </v-list-item>
                        
                    </v-row>
            </v-col><!--user image & name-->
        </v-row> <!--Review Title reating F-iconImg-->
        <hr>
        <v-row>
            <v-col justify="center" md="8" lg="8" xl="8" cols="12">
                <v-row>
                    <v-col cols="2" v-for="(image,i) in images"
                    :key="i"> 
                        <v-list-item-avatar color="grey darken-3">
                            <v-img
                                class="elevation-6"
                                src="../../../assets/Tourimage/asset 64.jpeg"
                            ></v-img>
                        </v-list-item-avatar>
                    </v-col><!-- User Avatar <loop 6times>-->
                </v-row>
                <v-row>
                    <p>+ 7 more travelers have enjoyed</p>
                    <p>the local experience with TakeMeTour Local Expert</p>
                </v-row>
                <v-row>
                    <v-btn class="ma-2 depressed white--text" color="indigo">50 reviews <v-icon>mdi-chevron-right</v-icon></v-btn>
                </v-row>
            </v-col>
        </v-row>
          <!-- </v-col>
          <v-col md="6" lg="6" xl="6" class="hidden-sm-and-down"></v-col>
      </v-row> -->
  </v-container>
</template>

<script>
export default {
    data:()=>({
        isActive1: false,
        isActive2: false,
        items: [
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me 2' },
        ],
        images:[
            {
                name:'asset 42.jpeg', txt:'Phuket'
            },
            {
                name:'asset 43.jpeg', txt:'Siem Reap'
            },
            {
                name:'asset 44.jpeg', txt:'Saigon'
            },
            {
                name:'asset 45.jpeg', txt:'Manila'
            }
            
        ]
    })
}
</script>

<style>
    @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .PopDesCrd{
        width: 125px!important;
        height: 125px!important;
        }
    }
</style>