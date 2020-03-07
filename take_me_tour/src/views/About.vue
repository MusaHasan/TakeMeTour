<template>
  <div class="about">
    <imageSlide/>
    <tourDetail/>
    <similiarExpe/>
    <SpecialPriceAtt/>
    <notExactly/>
    <bottomNavbar/>
  </div>
</template>
<script>
import imageSlide from '@/components/TourDetails/ImageSlider.vue'
import tourDetail from '@/components/TourDetails/StreetFoodTr.vue'
import similiarExpe from '@/components/TourDetails/SimiliarExp.vue'
import specialPriceAtt from '@/components/TourDetails/SpecialPriceAtt.vue'
import notExactly from '@/components/TourDetails/NotExactly.vue'
import bottomNavbar from '@/components/TourDetails/BottomNav.vue'

export default {
  components:{
    imageSlide,
    tourDetail,
    similiarExpe,
    bottomNavbar,
    notExactly,
    specialPriceAtt
  }
}
</script>
<style >

</style>
