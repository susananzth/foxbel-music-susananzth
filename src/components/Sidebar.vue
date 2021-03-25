<template>
        <div id="layoutSidebar">
            <nav class="sidenav shadow-right sidenav-light">
                <div class="sidenav-menu">
                    <img class="logo" src="../assets/foxbel-music.png" alt="Logo-Company">
                    <div class="sidenav-menu-heading">Mi Librería</div>
                    <a class="nav-link" href="#">Recientes</a>
                    <a class="nav-link" href="#">Artistas</a>
                    <a class="nav-link" href="#">Canciones</a>
                    <a class="nav-link" href="#">Estaciones</a>
                    <div class="sidenav-menu-heading pt-5">Playlist</div>
                    <a class="nav-link" href="#">Metal</a>
                    <a class="nav-link" href="#">Para bailar</a>
                    <a class="nav-link" href="#">Rock</a>
                    <a class="nav-link" href="#">Baladas</a>
                </div>
            </nav>
        </div>
</template>

<script scope>
export default {
  name: 'Sidebar',
}
</script>

<style scoped>
#layoutSidebar {
    height: auto;
    width: 30rem;
    z-index: 1038;
}
.sidenav{
    background: #662323;
    height: 100%;
    padding: 50px 0;

}
.logo{
    padding: 0 40px;
    padding-bottom: 30px;
    width: 100%;
}
.sidenav-menu-heading {
    color: #FFFFFF;
    font-size: 22px;
    font-weight: 700;
    line-height: 27px;
    padding-bottom: 4px;
    padding-left: 40px;
}
.nav-link {
    -webkit-box-align: center;
    align-items: center;
    color: #FFFFFF;
    display: -webkit-box;
    display: flex;
    font-size: 16px;
    font-weight: 300;
    line-height: 20px;
    padding: 4px 0;
    padding-bottom: 0.75rem;
    padding-left: 40px;
    position: relative;
}
.nav-link:hover {
    box-sizing: border-box;
    border-left: #E86060 solid 5px;
    color: #E86060;
    font-size: 16px;
    font-weight: 700;
    line-height: 20px;
    padding: 4px 0;
    padding-bottom: 0.75rem;
    padding-left: 35px;
    
}
</style>