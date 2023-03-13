<template>
    <div id="app">
    <NavBar/>  
    <OfferList/>
    <PageFooter/>
    </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import OfferList from './components/OfferList.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    OfferList,
    PageFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100%;
  margin: auto;
  background: linear-gradient(45deg, #0B1641 0%, #C70160 100%), #FFFFFF;;
}
</style>
