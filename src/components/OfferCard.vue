<template>
  <div class="card">
    <img :src="offer.thumb" alt="Deal Thumbnail" class="card-img-top" />

    <div class="card-body">
      <div class="card-title">
        <p>{{ offer.title }}</p>
      </div>
      <span class="card-container">
        <div class="details">
          <button
            target="_blank"
            rel="noopener noreferrer"
            @click="goToDetails(offer.dealID)"
          >
            DETALHES
          </button>
        </div>
        <div class="price-saving">
          <div class="prices">
            <s> &dollar; ({{ offer.normalPrice }})</s>
            <p>&dollar; {{ offer.salePrice }}</p>
          </div>
          <div id="saving-button">-{{ Math.round(offer.savings) }}%</div>
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
      if (dealID) {
        window.open(
          `https://www.cheapshark.com/redirect?dealID=${dealID}`,
          "_blank"
        )
      }
    },
  },
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}

.card {
  width: 15rem;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  margin-bottom: 1.8rem;
  margin-left: 2rem;
}

.card:hover {
  top: 2;
}

.card img {
  width: 15rem;

  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.card-body {
  height: 7.5rem;
  align-items: space-around;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: #0b1641;
  color: #ffffff;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
}

.card button {
  font-weight: bold;
  width: 6rem;
  height: 2rem;

  border-radius: 6px;
  font-family: "Bai Jamjuree", sans-serif;
  font-size: 0.9rem;
  color: #ffffff;
  margin-left: 0.6rem;
  margin-bottom: 1rem;
  background: #c70160;
  border: none;
  cursor: pointer;
  text-align: center;
}

.card button:hover {
  background: rgba(150, 3, 74, 0.843);
  transition: 0.5s;
  position: relative;
}

.card button:active {
  position: relative;
  top: 2px;
  box-shadow: none;
}

.card-title {
  display: flex;
  flex-direction: row;
  margin-left: 1rem;
  margin-top: 0.5rem;
  font-family: "Bai Jamjuree", sans-serif;
  font-size: 0.85rem;
  line-height: 20px;
  text-transform: uppercase;
  font-weight: 300;
  text-align: center;
}

#saving-button {
  background: #16857b;
  border-radius: 6px;
  width: 2.6rem;
  height: 1.9rem;

  color: #ffffff;
  justify-content: center;
  text-align: center;
  display: flex;
  flex-direction: column;
  font-weight: bold;
  font-size: 0.8rem;
  margin-top: auto;
  margin-bottom: 1rem;
  margin-right: 0.6rem;
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
  margin-right: 0.5rem;
}

.prices s {
  font-family: "Bai Jamjuree", sans-serif;
  font-style: normal;
  font-weight: 100;
  font-size: 0.6rem;
  line-height: 15px;
  text-align: right;
  text-decoration-line: line-through;
  color: #ffffff9f;
}

.prices p {
  font-family: "Bai Jamjuree", sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 0.7rem;
  line-height: 10px;
  text-align: right;
  color: #ffffff;
}
</style>
