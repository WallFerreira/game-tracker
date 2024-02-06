<template>
  <div class="navbar">
    <div class="navbar-icons">
      <img id="icone" src="../assets/Vector.svg" alt="" />
      <img id="logo" src="../assets/Game_Tracker.svg" alt="" />
    </div>
  </div>
</template>
<script>
export default {
  name: "nav-bar",
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
  background: #0b1641;
  height: 2.2rem;
  padding: 0.8rem;
}

#logo {
  display: flex;
  height: 1.2rem;
  margin-top: 0.7rem;
  margin-left: 1rem;

  justify-content: center;
}

#icone {
  display: flex;

  margin-left: 19.6rem;
}
</style>
