<template>
    <div class="container">
        <div> 
            <input class="seach-filter" type="search" placeholder="Procurar" icon="fa-solid fa-magnifying-glass" v-model="this.inputText" >
        </div>
        <div class="order-by">
            <p>Ordenar por: </p>
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

*{
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
}
.container {
    display: flex;
    margin-bottom: 2rem;

}
.seach-filter {
    display: flex;
    width: 380px;
    height: 50px;
    margin-top: 3rem;
    margin-right: 19em;
    padding: 12px;
    background: #0B1641;
    border-radius: 8px;
    color: #ffffff7b;
    border: none;
    font-size: medium;
}

.order-by {
    display: flex;
    flex-direction: row;
    justify-content: right;
    color: #FFFFFF;
    margin-left: 19.5em;

}

.order-by p {
    display: flex;
    color: #FFFFFF;
    margin-top: 3.5rem;
    font-weight: bold;
    align-items:center
    
}

.dropdown {
    display: flex;
    width: 180px;
    height: 50px;
    margin-top: 3rem;
    margin-left: 0.5rem;
    padding: 13px;
    padding-right: 2rem;
    background: #0B1641;
    color: #ffffff7b;
    border-radius: 8px;
    border: none;
    font-size: 1.08rem;
    align-items: center;

}

.dropdown option:hover {
    color: #C70160;
}
</style>

