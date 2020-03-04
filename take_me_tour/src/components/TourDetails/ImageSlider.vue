<template>
    <v-container fluid class="pa-0 imgBGblack">
        <v-container class="childContainer">
            <carousel 
                ref="test"
                class="slider"
                :perPage=1
                :navigationEnabled="true"
                :paginationEnabled="true"
                :autoplay="true"
                :loop="true"
            >
                <slide v-for="(image,i) in images" :key="i" transition="scale-transition">
                    <div class="card-image">
                        <figure class="image">
                            <img class="image" :src="require(`../../assets/Tourimage/${image.name}`)" alt="Image">
                        </figure>
                    </div>
                </slide>
            </carousel>
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
</style>