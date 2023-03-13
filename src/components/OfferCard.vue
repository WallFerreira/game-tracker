<template>
    <div class="card">
      <img :src="offer.thumb" alt="Deal Thumbnail" class="card-img-top">
      <div class="card-body">
        <h5 class="card-title">{{ offer.title }}</h5>
        <p class="card-text">{{ offer.salePrice }} ({{ offer.normalPrice }})</p>
        <a :href="offer.link" target="_blank" class="btn btn-primary">Go to deal</a>
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
    },
  };
  </script>
  
  <style scoped>
  .card {
    width: 18rem;
    margin-bottom: 1rem;
    justify-content: space-between;
    display: flex;
    flex-direction: column;
  }
  .card-body{
    color: #FFFFFF;
  }

  </style>
  