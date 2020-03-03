<template>
  <div class="about">
    <imageSlide/>
    <tourDetail/>
    <bottomNavbar/>
  </div>
</template>
<script>
import imageSlide from '@/components/TourDetails/ImageSlider.vue'
import tourDetail from '@/components/TourDetails/StreetFoodTr.vue'
import bottomNavbar from '@/components/TourDetails/BottomNav.vue'

export default {
  components:{
    imageSlide,
    tourDetail,
    bottomNavbar,
  }
}
</script>
<style >

</style>
