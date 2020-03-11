<template>
  <v-container>
      <div style="border-bottom: 1px solid #d0d0d0;"></div>
      <v-row>
        <v-col cols="12 pb-0">
            <p>If you're looking to taste the best street food in <span style="color:#1cb6e6">Bangkok</span>, then <span style="color:#1cb6e6">Bangkok</span> Chinatown is the place for you! 
                There's no better place than the world's biggest Chinatown to experience the mix of Thai and 
                Chinese culture, especially with your taste buds! Let our Local 
                Expert show you where the delicious hidden treasures are in the hidden alleys. Let's go!</p>
        </v-col>
      </v-row>
        <v-col cols="12 py-0">
            <customPlauer source="https://www.youtube.com/embed/FjeUQ87laNs"/>
        </v-col> <!--Youtube video sec-->
      <v-row>   

      </v-row>
  </v-container>
</template>

<script>
import customPlauer from './video'

export default {
  components:{
    customPlauer
  }
}
</script>

<style>

</style>