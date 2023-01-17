

<template>
  <section class="intro relative">           
    <Header></Header>
    <Banner></Banner>      
  </section>
  <brands></brands>
  <NewCollection></NewCollection>
  <BestSellers></BestSellers>
  <SpecialOffer></SpecialOffer>
</template>
<script >
import Header from '@/components/etalon/Header.vue'
import Banner from '@/components/etalon/Banner.vue'
import Brands from '@/components/etalon/Brands.vue'
import NewCollection from '@/components/etalon/NewCollection.vue'
import BestSellers from '@/components/etalon/BestSellers.vue'
import SpecialOffer from '@/components/etalon/SpecialOffer.vue'


export default{
  components: {
    Header,Banner,Brands,NewCollection,BestSellers,SpecialOffer
  },
  data (){
    return{

    }
  },
  methods: {

  }
}
</script>

<style scoped>

</style>