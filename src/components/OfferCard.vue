<template>
  <div class="card">
    <img :src="offer.thumb" alt="Deal Thumbnail" class="card-img-top">
    <div class="card-body">
      <div class="card-title">
        <p>{{ offer.title }}</p>
      </div>
      <span class="card-container">

        <div class="details">
          <button @click="goToDetails()">DETALHES</button>
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

  props: {
    offer: {
      type: Object,
      required: true,
    },
    methods: {
      goToDetails() {
        alert("clicou")

      },
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
  margin-bottom: 1rem;
  margin-left: 0.1rem;
  display: flex;
  flex-direction: column;
}

.card img {
  max-width: 100%;
  size: border-box;
  height: 60%;
  border-top-left-radius: 9px;
  border-top-right-radius: 9px;
}

.card-body {
  color: #FFFFFF;
  background: #0B1641;
  border-bottom-left-radius: 9px;
  border-bottom-right-radius: 9px;
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
  background: #C70160;
  border: none;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 18px;
  color: #FFFFFF;
  margin-left: 1.5rem;
  margin-bottom: 1rem;
}

.card button:hover {
  transform: scale(0.95);
  transition: all 0.3s;
}

.card-title {
  display: flex;
  flex-direction: row;
  margin-left: 1.5rem;
  margin-top: 0.5rem;
  font-family: 'roboto';
  font-size: 1.2rem;
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
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 100;
  font-size: 12px;
  line-height: 14px;
  /* identical to box height */

  text-align: right;
  text-decoration-line: line-through;

  color: #ffffff9f;
}

.prices p {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 700;
  font-size: 18px;
  line-height: 21px;
  /* identical to box height */

  text-align: right;

  color: #FFFFFF;

}
</style>
  