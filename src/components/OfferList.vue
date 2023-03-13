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
        "https://www.cheapshark.com/api/1.0/deals?pageNumber=0&pageSize=12&storeID=1&onSale=1&AAA=1"
      );
      this.offers = response.data;
    },
  };
  </script>
  