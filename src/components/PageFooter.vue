<template>
    <div class="page-footer">
        <div id="footer-icon">
            <img src="../assets/Vector.png" alt="">
        </div>
        
        <p id="footer-text">© 2021, Game Tracker Inc. Todos os direitos reservados. Nulla facilisi. Etiam sagittis congue
            tempor.
            Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
            Suspendisse eu velit et ante luctus egestas. Aenean sed nisi tellus. Duis non ornare libero.
            Quisque suscipit maximus nisi, in gravida felis. Cras ornare mauris ac nisi congue, ut condimentum sem
            tincidunt.
            Phasellus semper tellus malesuada turpis gravida cursus.
            Duis nec eleifend nunc, vitae finibus elit. Aliquam eget diam vitae purus suscipit viverra.
        </p>
        <div style="text-decoration: none;" id="footer-link">
            <a href="">Termos de Serviço</a>
            <a href="">Politica de Privacidade</a>
            <a href="">Trabalhe conosco</a>
            <a href="">Contato</a>
        </div>

    </div>
</template>
<script>
export default {

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
    background: #0B1641;
    justify-content: center;
    height: 20rem;
    padding: 8rem;
    align-items: center;
}

#footer-text {
    display: flex;
    justify-content: center;
    color: #FFFFFF;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;

}

#footer-link {
    display: flex;
    color: #FFFFFF;
    margin-bottom: 2px;
    font-weight: bold;
    margin: 12rem;

}

#footer-icon {
    display: flex;
    margin: 0;
}
</style>