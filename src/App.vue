<template>
  <div id="app">
    <NavBar />
    <OfferFilter />
    <OfferList />
    <PageFooter />
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue"
import OfferList from "./components/OfferList.vue"
import PageFooter from "./components/PageFooter.vue"
import OfferFilter from "./components/OfferFilter.vue"

export default {
  name: "App",
  components: {
    NavBar,
    OfferList,
    PageFooter,
    OfferFilter,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: linear-gradient(100deg, #0b1641 0%, #c70160 100%), #ffffff;
  align-content: center;
  justify-content: center;
  background-size: auto;
  display: flex;
  flex-direction: column;
  min-width: 1240px;
}
</style>
