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
import axios from "axios"
import OfferCard from "@/components/OfferCard.vue"

export default {
  name: "offer-list",

  components: {
    OfferCard,
  },

  data() {
    return {
      offers: [],
    }
  },

  async created() {
    const response = await axios.get(
      "https://www.cheapshark.com/api/1.0/deals?pageNumber=0&pageSize=16&storeID=3&onSale=3&AAA=1"
    )
    this.offers = response.data
  },
}
</script>
<style>
.container {
  display: flex;
  margin: 1rem;
  justify-content: center;
}

.row {
  columns: 4;
}
</style>
