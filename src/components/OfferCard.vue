<template>
  <div class="card">
    <img :src="offer.thumb" alt="Deal Thumbnail" class="card-img-top">
    <div class="card-body">
      <div class="card-title">
        <p>{{ offer.title }}</p>
      </div>
      <span class="card-container">

        <div class="details">
          <button target="_blank" rel="noopener noreferrer" @click="goToDetails(offer.dealID)">DETALHES</button>
        </div>
        <div class="price-saving">
          <div class="prices">
            <s> &dollar; ({{ offer.normalPrice }})</s>
            <p> &dollar; {{ offer.salePrice }}</p>
          </div>
          <div id="saving-button">
            -{{ Math.round(offer.savings) }}%
          </div>
        </div>
      </span>
    </div>
  </div>
</template>
  
<script>
export default {
  name: "offer-card",

  props: {
    offer: {
      type: Object,
      required: true,
    },
  },
  methods: {
    goToDetails(dealID) {
      window.location.href = `https://www.cheapshark.com/redirect?dealID=${dealID}`
    },
  },

};
</script>
  
<style scoped>
* {
  margin: 0;
  padding: 0;
}

.card {
  width: 26rem;
  height: 18rem;
  margin-left: 0.1rem;
  display: flex;
  flex-direction: column;

}

.card img {
  max-width: 100%;
  size: border-box;
  height: 50%;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.card-body {
  color: #FFFFFF;
  background: #0B1641;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  height: 40%;
  align-items: space-around;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}


.card button {
  font-weight: bold;
  width: 116px;
  height: 39px;
  border-radius: 8px;
  font-family: 'Bai Jamjuree', sans-serif;
  font-size: 18px;
  color: #FFFFFF;
  margin-left: 1.5rem;
  margin-bottom: 1rem;
  background: #C70160;
  border: none;
  box-shadow: 0px 0px 5px -1px
}

.card button:hover {
  background: rgba(150, 3, 74, 0.843);
  transition: .5s;

}

.card-title {
  display: flex;
  flex-direction: row;
  margin-left: 1.5rem;
  margin-top: 0.5rem;
  font-family: 'Bai Jamjuree', sans-serif;
  font-size: 1.3rem;
  line-height: 28px;
}

#saving-button {
  background: #16857B;
  border-radius: 8px;
  width: 84px;
  height: 39px;
  color: #FFFFFF;
  justify-content: center;
  text-align: center;
  display: flex;
  flex-direction: column;
  font-weight: bold;
  font-size: larger;
  margin-top: auto;
  margin-bottom: 1rem;
  margin-right: 1.5rem;
}

.card-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.price-saving {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.details {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.prices {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-right: 1rem;
}

.prices s {
  font-family: 'Bai Jamjuree', sans-serif;
  font-style: normal;
  font-weight: 100;
  font-size: 12px;
  line-height: 14px;
  text-align: right;
  text-decoration-line: line-through;
  color: #ffffff9f;
}

.prices p {
  font-family: 'Bai Jamjuree', sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 18px;
  line-height: 21px;
  text-align: right;
  color: #FFFFFF;
}
</style>
  