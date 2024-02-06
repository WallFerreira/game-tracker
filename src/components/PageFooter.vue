<template>
  <div class="page-footer">
    <div id="footer-icon">
      <img src="../assets/Vector.svg" alt="" />
    </div>

    <p id="footer-text">
      © 2021, Game Tracker Inc. Todos os direitos reservados. Nulla facilisi.
      Etiam sagittis congue tempor. Pellentesque habitant morbi tristique
      senectus et netus et malesuada fames ac turpis egestas. Suspendisse eu
      velit et ante luctus egestas. Aenean sed nisi tellus. Duis non ornare
      libero. Quisque suscipit maximus nisi, in gravida felis. Cras ornare
      mauris ac nisi congue, ut condimentum sem tincidunt. Phasellus semper
      tellus malesuada turpis gravida cursus. Duis nec eleifend nunc, vitae
      finibus elit. Aliquam eget diam vitae purus suscipit viverra.
    </p>
    <div id="footer-link">
      <a href="">Termos de Serviço</a>
      <a href="">Politica de Privacidade</a>
      <a href="">Trabalhe conosco</a>
      <a href="">Contato</a>
    </div>
  </div>
</template>
<script>
export default {
  name: "page-footer",
}
</script>
<style>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
}

.page-footer {
  background: #0b1641;
  justify-content: center;
  height: 11rem;
  padding: 7rem;
  align-items: center;
}

#footer-icon {
  display: flex;
  justify-content: center;
  margin-bottom: 2rem;
}

#footer-text {
  display: flex;
  justify-content: center;
  align-content: flex-start;
  margin: 0 10rem 0 10rem;
  color: #ffffff9f;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}

#footer-link {
  display: flex;
  justify-items: flex-start;
  color: #ffffff;
  margin-bottom: 2px;
  font-weight: bold;
  margin-top: 3rem;
  margin-left: 8rem;
}

#footer-link a {
  margin-left: 2rem;
  color: #ffffff;
}
</style>
