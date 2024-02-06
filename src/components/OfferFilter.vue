<template>
  <div class="container">
    <input
      class="seach-filter"
      type="search"
      placeholder="Procurar"
      icon="fa-solid fa-magnifying-glass"
      v-model="this.inputText"
    />

    <div class="order-by">
      <p>Ordenar por:</p>
      <select v-model="selectedOption" class="dropdown" type="dropdown">
        <option value="">% de desconto</option>
        <option value="">Maior preço</option>
        <option value="">Menor preço</option>
        <option value="">Título</option>
      </select>
    </div>
  </div>
</template>
<script>
export default {
  name: "offer-filter",
  data() {
    return {
      inputText: "",
      selectedOption: "",
    }
  },
}
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
}
.container {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin: 3rem auto; /* Definindo margem apenas nas laterais */
  max-width: 1750px; /* Limitando a largura máxima do container */
  gap: 15rem;
}
.seach-filter {
  display: flex;
  width: 380px;
  height: 50px;

  padding: 12px;
  background: #0b1641;
  border-radius: 8px;
  color: #ffffff7b;
  border: none;
  font-size: medium;
  align-items: center;
  margin: 0 0 0 21rem;
  max-width: 100%;
}

.order-by {
  display: flex;
  color: #ffffff;
  align-content: center;
  margin: 0 19rem 0 0;
  align-self: center; /* Alinhando verticalmente */
}

.order-by p {
  display: flex;
  color: #ffffff;
  font-weight: bold;
  align-items: center;
}

.dropdown {
  display: flex;
  width: 180px;
  height: 50px;
  margin-left: 0.5rem;
  padding: 13px;
  padding-right: 2rem;
  background: #0b1641;
  color: #ffffff7b;
  border-radius: 8px;
  border: none;
  font-size: 1.08rem;
}

.dropdown option:hover {
  background-color: #c70160;
}
</style>
