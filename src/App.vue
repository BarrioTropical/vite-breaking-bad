<template>

    
  <HeaderComponent/>
  <main>
  <div class="container">
  <SearchBarComponent/>
  <MainComponent/>
  <ProductListComponent/>
  </div> 
  </main>


</template>

<script>
import axios from 'axios';
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import SearchBarComponent from './components/SearchBarComponent.vue';
import ProductListComponent from './components/ProductListComponent.vue'

  export default {
    components: { HeaderComponent, MainComponent, SearchBarComponent, ProductListComponent },

}
</script>

<style lang="scss" scoped>
  
</style>