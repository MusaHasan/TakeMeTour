<template>
  <div class="home">
    <backgroundVdo/>
    <getInspired/>
    <tourAvailable/>
    <findTour/>
    <travelProduct/>
    <takeMeTour/>
    <popularDestination/>
    <travelersReview/>

  </div>
</template>

<script>
// @ is an alias to /src
import backgroundVdo from '@/components/HomeComponents/BackVideo.vue'
import getInspired from '@/components/HomeComponents/GetInspired.vue'
import tourAvailable from '@/components/HomeComponents/ToursAvailable.vue'
import findTour from '@/components/HomeComponents/FindTour.vue'
import travelProduct from '@/components/HomeComponents/TravelProduct.vue'
import takeMeTour from '@/components/HomeComponents/TakeMeTour.vue'
import popularDestination from '@/components/HomeComponents/PopularDestination.vue'
import travelersReview from '@/components/HomeComponents/TravelersReview.vue'

export default {
  name: 'Home',
  components: {
    backgroundVdo,
    getInspired,
    tourAvailable,
    findTour,
    travelProduct,
    takeMeTour,
    popularDestination,
    travelersReview
  }
}
</script>
<style >
  .v-slide-group__prev, .v-slide-group__next{
    flex: 0 1 34px!important;
    min-width: 27px!important;
    background-color: #fffafa00;
  }
</style>
