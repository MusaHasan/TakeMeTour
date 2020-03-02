<template>
  <div class="home">
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
import getInspired from '@/components/GetInspired.vue'
import tourAvailable from '@/components/ToursAvailable.vue'
import findTour from '@/components/FindTour.vue'
import travelProduct from '@/components/TravelProduct.vue'
import takeMeTour from '@/components/TakeMeTour.vue'
import popularDestination from '@/components/PopularDestination.vue'
import travelersReview from '@/components/TravelersReview.vue'

export default {
  name: 'Home',
  components: {
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
