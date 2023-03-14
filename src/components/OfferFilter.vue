<template>
    <div>
        <form action="">
            <input class="seach-filter" type="text" label="Procurar">
            <i icon="fa-solid fa-magnifying-glass"></i>
        </form>
    </div>
</template>
<script>
export default {
    name: "offer-filter"

}
</script>
<style>

.seach-filter {
    display: flex;
    width: 380px;
    height: 40px;
    margin-top: 3rem;
    margin-left: 3rem;
    padding: 12px;
    background: #0B1641;
    border-radius: 8px;
    color: #FFFFFF;
    border: none;
    font-size: medium;
}
</style>

