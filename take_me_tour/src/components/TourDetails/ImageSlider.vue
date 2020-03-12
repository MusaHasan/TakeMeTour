<template>
    <v-container fluid class="pa-0 imgBGblack">
        <v-container class="childContainer">
            <carousel 
                ref="test"
                class="slider"
                :perPage=1
                :navigationEnabled="true"
                :paginationEnabled="true"
                paginationActiveColor="orange"
                :autoplay="true"
                :loop="true"
            >
                <slide  v-for="(image,i) in images" :key="i" transition="scale-transition">
                    <div class="card-image">
                        <figure class="image">
                            <img class="image" :src="require(`../../assets/Tourimage/${image.name}`)" alt="Image">
                        </figure>
                    </div>
                </slide>
                
            </carousel>
           <v-row class="upperIcons hidden-md-and-up">
               <v-col cols="2"> <v-icon class="left" color="white">mdi-chevron-left</v-icon> </v-col>
               <v-col cols="8"></v-col>
               <v-col class="px-0" cols="2">
                    <v-icon class="share" color="white">mdi-arrow-up-bold-box-outline</v-icon>
                    <v-icon class="heart" color="white">mdi-heart-outline</v-icon>
                    <v-icon class="right" color="white">mdi-chevron-right</v-icon>
                </v-col>
               
               
                
            </v-row>
        </v-container>
    </v-container>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
export default {
    components:{
        Carousel,
        Slide
    },
    data:()=>({
        imgUrl:'../../assets/Tourimage/',
        images:[
            { name: 'asset 4.jpg'},
            { name: 'asset 5.jpg'},
            { name: 'asset 6.jpg'},
            { name: 'asset 7.jpg'},
            { name: 'asset 8.jpg'},
            { name: 'asset 9.jpg'},
        ],
    }),
    mounted() {
        setTimeout(() => {
            this.$refs['test'].onResize();
            this.$refs['test'].goToPage(0);
        }, 200);
    }
}
</script>

<style>
 .image{
    width: 100%;
    }
    .VueCarousel-inner{
        transition: opacity 1s ease-in-out 0s!important;
    }
    .slider{
        margin: -10px 0;
    }
    .VueCarousel-pagination[data-v-438fd353]{
        margin: -46px 0!important;
    }
    .title{
        color:turquoise;
        font-size: 1rem;
        font-weight: 400;
    }
    .imgBGblack{
        background-color: black;
}
@media only screen and (min-width: 1264px) 
  and ( max-width: 2000px){
  .slider{

      padding: 13px 0;
  }
}
@media only screen and (min-device-width : 320px)
        and (max-device-width : 767px) {
    
    
    .slider{
        margin: 0px 16px;
        padding-bottom: 23px;
    }
    
    .imgBGblack .childContainer{
        margin-top: 42px;
        padding: 0 0;
    }
    .upperIcons{
        width: 100%;
        height: 200px;
        position:absolute;
        top: 56px;
        background: linear-gradient(to bottom, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.45) 1%, rgba(18,17,18,0.1) 20%, rgba(36,35,36,0.05) 21%, rgba(237,237,237,0.05) 32%);   
    }

    .upperIcons .left{
        top: 75px;
        left: -3px;
        font-size: 55px;
    }
    .upperIcons .share{
        top: -8px;
        left: -15px;
        font-size: 25px;
    }
    .upperIcons .heart{
        top: -8px;
        font-size: 25px;
    }
    .upperIcons .right{
        top: 48px;
        right: -27px;
        font-size: 55px;
    }
    .VueCarousel-dot{
        padding: 4px!important;
    }
}
@media only screen and (max-device-width: 360px)
 {
   .slider{
        margin: 3px 0;
        padding-bottom: 23px;
    }
    .upperIcons .left{
        top: 70px;
        left: -3px;
        font-size: 55px;
    }
    .upperIcons .right{
        top: 42px;
        right: -14px;
        font-size: 55px;
    }
}
@media only screen and (max-device-width: 320px)
 {
   .slider{
        margin: 3px 0;
        padding-bottom: 23px;
    }
    .upperIcons .left{
        top: 68px;
        left: -3px;
        font-size: 55px;
    }
    .upperIcons .right{
        top: 38px;
        right: -14px;
        font-size: 55px;
    }
}
</style>