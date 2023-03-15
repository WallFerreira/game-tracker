<template>
    <div class="navbar">
        <div class="navbar-icons">
            <img id="icone" src="../assets/Vector.svg" alt="">
            <img id="logo" src="../assets/Game_Tracker.svg" alt="">
        </div>
    </div>
</template>
<script>
export default {
    name: "nav-bar"

}
</script>
<style scoped>
* {
    margin: 0;
    padding: 0;
    list-style: none;
    text-decoration: none;
}
.navbar-icons {
    display: flex;
    align-content: space-between;
    background: #0B1641;
    height: 2rem;
    padding: 0.3rem
}

#logo {
    display: flex;
    height: 1rem;
    margin-top: 0.5rem;
    margin-left: 1rem;

    justify-content: center;
}

#icone {
    display: flex;
    
    margin-left: 19.6rem;
}
</style>