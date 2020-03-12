<template>
  <v-container class="py-0">
      
        <v-row >
            <v-col class="py-0" md="7" lg="7" xl="7" cols="12" >
                <div class="d-flex">
                    <h3 class="mt-3 d-flex">Reviews <p class="ml-1 mt-1">(50)</p></h3> 
                    <v-spacer/>
                    <v-rating
                        color="yellow darken-3"
                        background-color="yellow darken-3"
                        empty-icon="$ratingFull"
                        class="py-3 pr-2"
                    ></v-rating> <span class="mt-3">4.7</span> 
                </div>

                <v-list class="mx-0 mt-4">
                    <v-list-item class="px-0" style="margin: -27px 0" v-for="(item,i) in items" :key="i" >
                        <v-list-item-content class="py-0 reatingTxt">
                        <v-list-item-subtitle style="padding-right: 113px" > <p>Friendliness</p>  </v-list-item-subtitle>
                        </v-list-item-content>

                        <v-list-item-icon class="pl-12 my-0 ml-12"> 
                            <v-rating
                                color="yellow darken-3"
                                background-color="yellow darken-3"
                                empty-icon="$ratingFull"
                                class="mt-1 pr-2 mx-2 reating"
                            ></v-rating> 
                        </v-list-item-icon>
                        <v-list-item-content class="pa-0">
                        <v-list-item-subtitle> <p>4.8</p>  </v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>

                <div class="d-lg-flex d-md-flex d-xl-flex d-block"> <!--Review Buttons-->
                    <v-menu  offset-y>
                        <template v-slot:activator="{ on }">
                            <v-hover v-slot:default="{ hover }">
                                <v-btn
                                class="active allCountries mr-1 mb-1 mt-2 mt-md-10 mt-lg-10 mt-xl-10"
                                height="34"
                                width="202"
                                :ripple="false"
                                light
                                v-on="on"
                                @click="isActive1=!isActive1"
                                outlined
                                :elevation="hover ? 6 : 0"
                                :class="{ 'on-hover': hover, activeBtn1 : isActive1 }"
                                >
                                   <v-img src="../../../assets/Tourimage/asset 51.png"></v-img> <span class=" mx-1 mr-2 mr-md-8 mr-lg-8 mr-xl-8">All Countries</span><v-icon color="grey darken-4">mdi-menu-down</v-icon>
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
                    </v-menu> <!--Btn1-->

                    <v-menu  offset-y>
                        <template v-slot:activator="{ on }">
                            <v-hover v-slot:default="{ hover }">
                                <v-btn
                                class="active sortRecent ml-1 mb-1 mt-2 mt-md-10 mt-lg-10 mt-xl-10"
                                height="34"
                                width="202"
                                :ripple="false"
                                light
                                v-on="on"
                                @click="isActive1=!isActive1"
                                outlined
                                :elevation="hover ? 6 : 0"
                                :class="{ 'on-hover': hover, activeBtn1 : isActive1 }"
                                >
                                    <span class="mr-4 mr-md-10 mr-lg-10 mr-xl-10">Sort:mostRec.</span><v-icon color="grey darken-1">mdi-swap-vertical</v-icon>
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
                    </v-menu> <!--Btn2-->
                </div>
            </v-col>
            <v-col cols="5" class="hidden-sm-and-down"></v-col>
            
        </v-row> <!--Reatings Button-->

        <v-row class="RvwImgRow1">
            <v-col class="RvwImgCol1" cols="3" v-for="(image,i) in images"
                :key="i">
                <v-card
                    class="my-1 RvwImgCrd"
                    height="128"
                    width="128"
                    :ripple="false"
                >
                    <v-img
                        class="white--text img align-end"
                        height="100%"
                        :src="require(`../../../assets/images/${image.name}`)"
                    >                    
                    </v-img>
                </v-card>
            </v-col> <!--Review images -->
            <v-col cols="2" class="RvwImgCol1" >
                <v-card
                    class="ma-1 RvwImgCrd"
                    height="128"
                    width="50"
                    :ripple="false"
                >
                    <v-icon class="threeDot">mdi-dots-horizontal</v-icon>
                </v-card>
            </v-col><!--images icon card-->
        </v-row><!--Review Images-->
        
        <v-row>
            <v-col class="hidden-md-and-up pa-0" md="4" lg="4" xl="4" cols="12">
                <v-row>
                    <v-list-item class="grow ">
                        <v-col class="pa-0 avatarIcon" cols="2"> 
                            <v-list-item-avatar color="grey darken-3">
                                <v-img
                                    class="elevation-6"
                                    src="../../../assets/Tourimage/asset 64.jpeg"
                                ></v-img>
                            </v-list-item-avatar>
                        </v-col>
                        <v-col class="pa-0" cols="12">
                            <v-list-item-content class="pb-0">
                                <v-list-item-title>Hannah S.</v-list-item-title>
                                <v-list-item-title>
                                    <p>February 19, 2020 </p> 
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-col>
                    </v-list-item>
                    
                </v-row>
            </v-col><!--user image & name-->

            <v-col class="py-0 py-md-3 py-lg-3 py-xl-3" md="8" lg="8" xl="8" cols="12"><!--title txt-->
                <h3>Street Food Tour in Bangkok Chinatown</h3>
                <div class="d-flex">
                    <v-rating
                    color="yellow darken-3"
                    background-color="yellow darken-3"
                    empty-icon="$ratingFull"
                    class="mr-2"
                    ></v-rating> 4.8
                </div>
                <p>Eddie was very friendly, kind & knowledgeable of the Chinatown neighborhood. Being a native of 
                    Bangkok, he took me to some local favorite eateries that were very savory. It was great 
                    to have a local navigate me through this very exciting but busy area.
                        At the end we had a refreshing traditional Thai dessert :) It was an enjoyable experience.
                </p>
                <v-row class="RvwImgRow2">
                    <v-col class="RvwImgCol2" cols="4">
                        <v-card
                            class="my-1 RvwImgCrd2"
                            :ripple="false"
                        >
                            <v-img
                                class="white--text img align-end"
                                height="100%"
                                src="../../../assets/images/asset 42.jpeg"
                            >                    
                            </v-img>
                        </v-card>
                    </v-col> <!--Review images <loop 4 times>-->
                    <v-col class="RvwImgCol2" cols="4">
                        <v-card
                            class="my-1 RvwImgCrd2"
                            :ripple="false"
                        >
                            <v-img
                                class="white--text img align-end"
                                height="100%"
                                src="../../../assets/images/asset 42.jpeg"
                            >                    
                            </v-img>
                        </v-card>
                    </v-col> <!--Review images <loop 4 times>-->
                    <v-col class="RvwImgCol2" cols="4">
                        <v-card
                            class="my-1 RvwImgCrd2"
                            :ripple="false"
                        >
                            <v-img
                                class="white--text img align-end"
                                height="100%"
                                src="../../../assets/images/asset 42.jpeg"
                            >
                                <v-row class="img_1_BG">
                                    <v-col style="background-color:#000000bd;">
                                         <h5 style="font-size: 23px;" class="mt-7 ml-4 ml-md-8 ml-lg-8 ml-xl-8 white-text"><v-icon color="white">mdi-plus</v-icon> 1</h5>
                                    </v-col>
                                </v-row>                   
                            </v-img>
                        </v-card>
                    </v-col> <!--Review images <loop 4 times>-->
                </v-row><!--Review 3 Images-->
                <p style="font-size:10px!important">
                    Helpful? <v-icon class="px-2" color="rgb(161, 173, 179)" style="font-size:16px!important; border-right: 1px solid #425e6c;">mdi-thumb-up-outline</v-icon> <v-icon class="px-2" color="rgb(161, 173, 179)" style="font-size:16px!important;">mdi-thumb-down-outline</v-icon>
                </p>
            </v-col>
            
            <v-col class="hidden-sm-and-down pt-0" md="4" lg="4" xl="4" cols="12">
                <v-row>
                    <v-list-item class="grow">
                        <v-col class="mb-5" cols="3"> 
                            <v-list-item-avatar color="grey darken-3">
                                <v-img
                                    class="elevation-6"
                                    src="../../../assets/Tourimage/asset 64.jpeg"
                                ></v-img>
                            </v-list-item-avatar>
                        </v-col>
                        <v-col cols="9">
                            <v-list-item-content>
                                <v-list-item-title>Hannah S.</v-list-item-title>
                                <v-list-item-title>
                                    <p>February 19, 2020 </p> 
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-col>
                    </v-list-item>
                    
                </v-row>
            </v-col><!--user image & name-->
        </v-row> <!--Review Title reating F-iconImg-->

        <div style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->

        <v-row>
            <v-col class="hidden-md-and-up pa-0" md="4" lg="4" xl="4" cols="12">
                <v-row>
                    <v-list-item class="grow ">
                        <v-col class="pa-0 avatarIcon" cols="2"> 
                            <v-list-item-avatar color="grey darken-3">
                                <v-img
                                    class="elevation-6"
                                    src="../../../assets/Tourimage/asset 64.jpeg"
                                ></v-img>
                            </v-list-item-avatar>
                        </v-col>
                        <v-col class="pa-0" cols="10">
                            <v-list-item-content class="pb-0">
                                <v-list-item-title>Hannah S.</v-list-item-title>
                                <v-list-item-title>
                                    <p>February 19, 2020 </p> 
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-col>
                    </v-list-item>
                    
                </v-row>
            </v-col><!--user image & name-->
            <v-col class="py-0 py-md-3 py-lg-3 py-xl-3" md="8" lg="8" xl="8" cols="12"><!--title txt-->
                <h3>Street Food Tour in Bangkok Chinatown</h3>
                <div class="d-flex">
                    <v-rating
                    color="yellow darken-3"
                    background-color="yellow darken-3"
                    empty-icon="$ratingFull"
                    class="mr-2"
                    ></v-rating> 4.8
                </div>
                <p>Eddie was very friendly, kind & knowledgeable of the Chinatown neighborhood. Being a native of 
                    Bangkok, he took me to some local favorite eateries that were very savory. It was great 
                    to have a local navigate me through this very exciting but busy area.
                        At the end we had a refreshing traditional Thai dessert :) It was an enjoyable experience.
                </p>
                <p style="font-size:10px!important">
                    Helpful? <v-icon class="px-2" color="rgb(161, 173, 179)" style="font-size:16px!important; border-right: 1px solid #425e6c;">mdi-thumb-up-outline</v-icon> <v-icon class="px-2" color="rgb(161, 173, 179)" style="font-size:16px!important;">mdi-thumb-down-outline</v-icon>
                </p>
            </v-col>
            <v-col class="hidden-sm-and-down pt-0" md="4" lg="4" xl="4" cols="12">
                    <v-row>
                        <v-list-item class="grow">
                            <v-col class="mb-5" cols="3"> 
                                <v-list-item-avatar color="grey darken-3">
                                    <v-img
                                        class="elevation-6"
                                        src="../../../assets/Tourimage/asset 64.jpeg"
                                    ></v-img>
                                </v-list-item-avatar>
                            </v-col>
                            <v-col cols="9">
                                <v-list-item-content>
                                    <v-list-item-title>Hannah S.</v-list-item-title>
                                    <v-list-item-title>
                                        <p>February 19, 2020 </p> 
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-col>
                        </v-list-item> 
                    </v-row>
            </v-col><!--user image & name-->
        </v-row> <!--Review Title reating F-iconImg-->

       <div style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->

        <v-row>
            <v-col class="hidden-md-and-up pa-0" md="4" lg="4" xl="4" cols="12">
                <v-row>
                    <v-list-item class="grow ">
                        <v-col class="pa-0 avatarIcon" cols="2"> 
                            <v-list-item-avatar color="grey darken-3">
                                <v-img
                                    class="elevation-6"
                                    src="../../../assets/Tourimage/asset 64.jpeg"
                                ></v-img>
                            </v-list-item-avatar>
                        </v-col>
                        <v-col class="pa-0" cols="10">
                            <v-list-item-content class="pb-0">
                                <v-list-item-title>Hannah S.</v-list-item-title>
                                <v-list-item-title>
                                    <p>February 19, 2020 </p> 
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-col>
                    </v-list-item>
                    
                </v-row>
            </v-col><!--user image & name-->
            <v-col class="py-0 py-md-3 py-lg-3 py-xl-3" md="8" lg="8" xl="8" cols="12"><!--title txt-->
                <h3>Street Food Tour in Bangkok Chinatown</h3>
                <div class="d-flex mb-10">
                    <v-rating
                    color="yellow darken-3"
                    background-color="yellow darken-3"
                    empty-icon="$ratingFull"
                    class="mr-2"
                    ></v-rating> 4.8
                </div>
                <p style="font-size:10px!important">
                    Helpful? <v-icon class="px-2" color="rgb(161, 173, 179)" style="font-size:16px!important; border-right: 1px solid #425e6c;">mdi-thumb-up-outline</v-icon> <v-icon class="px-2" color="rgb(161, 173, 179)" style="font-size:16px!important;">mdi-thumb-down-outline</v-icon>
                </p>
            </v-col>
            <v-col class="hidden-sm-and-down pt-0" md="4" lg="4" xl="4" cols="12">
                    <v-row>
                        <v-list-item class="grow">
                            <v-col class="mb-5" cols="3"> 
                                <v-list-item-avatar color="grey darken-3">
                                    <v-img
                                        class="elevation-6"
                                        src="../../../assets/Tourimage/asset 64.jpeg"
                                    ></v-img>
                                </v-list-item-avatar>
                            </v-col>
                            <v-col cols="9">
                                <v-list-item-content>
                                    <v-list-item-title>Hannah S.</v-list-item-title>
                                    <v-list-item-title>
                                        <p>February 19, 2020 </p> 
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-col>
                        </v-list-item> 
                    </v-row>
            </v-col><!--user image & name-->
        </v-row> <!--Review Title reating F-iconImg-->

        <div style="border-bottom: 1px solid #d0d0d0;"></div><!--Line break-->
        

        <v-row justify="center">
            <v-col  md="10" lg="10" xl="10" cols="12">
                <v-row class="userAvatarRow" justify="center">
                    <v-col class="px-0 mx-2" cols="1" v-for="(user,i) in Users"
                    :key="i"> 
                        <v-list-item-avatar class="Useravatar" color="grey darken-3">
                            <v-img
                                class="elevation-6"
                                :src="require(`../../../assets/Tourimage/${user.name}`)"
                            ></v-img>
                        </v-list-item-avatar>
                    </v-col><!-- User Avatar <loop 6times>-->
                </v-row>
                <v-row justify="center">
                    <div class="text-center">
                    <p>+ 7 more travelers have enjoyed</p>
                    <p>the local experience with TakeMeTour Local Expert</p>
                    <v-btn class="ma-2 depressed "  outlined color="grey lighten-1"><span style="color:#1CB6E6">More reviews</span> </v-btn>
                    </div>
                </v-row>
            </v-col>
        </v-row> <!--User avatar-->
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
            
        ],
        Users:[
            {
                name:'asset 67.png', txt:'Phuket'
            },
            {
                name:'asset 68.jpeg', txt:'Siem Reap'
            },
            {
                name:'asset 69.jpeg', txt:'Saigon'
            },
            {
                name:'asset 70.jpeg', txt:'Manila'
            },
            {
                name:'asset 71.jpeg', txt:'Saigon'
            },
            {
                name:'asset 72.jpeg', txt:'Saigon'
            },
            {
                name:'asset 73.png', txt:'Saigon'
            }
            
        ]
    })
}
</script>

<style>
    .reating .v-icon{
        font-size: 12px!important;
        }
        .miniReating{
            margin: -10px 0;
        }
        .reatingTxt{
            padding-right: 190px;
        }
        .RvwImgRow1{
            padding-left: 27px;
        }
        .RvwImgCol1{
            margin: 0 -24px;
        }
        .RvwImgRow2{
            padding-left: 10px;
        }
        .threeDot{
            padding: 12px;
            margin: 48px 0;
        }
        .RvwImgCol2{
            margin: 0 -16px;
        }
        .RvwImgCrd2{
            height: 128px;
            width: 128px;
    }
    .img_1_BG{
        height: 132px;
    }
    .userAvatarRow{
        margin: 0 65px;
    }
    .Useravatar{
        height: 50px!important;
        width: 50px!important;
        min-width: 50px!important;
    }
    @media only screen
    and (min-device-width : 320px)
    and (max-device-width : 767px) {
        .RvwImgCrd{
        width: 60px!important;
        height: 60px!important;
        }
        .reatingTxt {
            padding-right: 120px;
        }
        .RvwImgRow1 {
            padding-left: 8px;
        }
        .RvwImgCol1 {
            margin: 0 -8px;
        }

        .RvwImgCrd2 {
            height: 112px;
            width: 112px;
        }
        .threeDot {
            margin: 18px 0;
            padding: 0 6px;
        }
        .RvwImgCol2 {
            margin: 0 -4px;
        }
        .userAvatarRow{
            margin: 0 20px;
        }
        .Useravatar{
            height: 36px!important;
            width: 36px!important;
            min-width: 36px!important;
        }
        .img_1_BG{
            height: 113px;
            
        }
        .allCountries{
            width: 183px!important;
        }
        .sortRecent{
            width: 183px!important;
        }
        .avatarIcon .v-list-item__avatar{
            margin-top: -6px;
            margin-left: 10px;
        }
    }
</style>