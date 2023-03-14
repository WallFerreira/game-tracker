<template>
  <div id="app">
    <NavBar />
    <OfferFilter/>
    <OfferList />
    <PageFooter />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import OfferList from './components/OfferList.vue';
import PageFooter from './components/PageFooter.vue';
import OfferFilter from './components/OfferFilter.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    OfferList,
    PageFooter,
    OfferFilter
    
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background: linear-gradient(45deg, #0B1641 0%, #C70160 100%), #FFFFFF;
  align-content: center;
  justify-content: center;
  background-size: 100%;
  background-position: cover
}
</style>
