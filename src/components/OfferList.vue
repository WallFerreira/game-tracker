<template>
    <div class="container">
      <div class="row">
        <div class="col" v-for="offer in offers" :key="offer.dealID">
          <offer-card :offer="offer" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import axios from "axios";
  import OfferCard from "@/components/OfferCard.vue";
  
  export default {
    components: {
      OfferCard
    },
    data() {
      return {
        offers: [],
      };
    },
    async created() {
      const response = await axios.get(
        "https://www.cheapshark.com/api/1.0/deals?storeID=1&upperPrice=20"
      );
      this.offers = response.data;
    },
  };
 </script>
<style>

  .container{
    margin: 10rem;
    display: flex;
    justify-content: center;
  }

  .row{
    columns: 3;
  }
</style>
  