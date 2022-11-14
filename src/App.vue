<template>

    
  <HeaderComponent/>
  <main>
  <MainComponent/>
  </main>


</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';

  export default {
    components: { HeaderComponent, MainComponent }
}
</script>

<style lang="scss" scoped>
  body{
    height: 100vh;
    background-color: #2E3A46;
  }
</style>