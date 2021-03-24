<template>
        <div id="layoutSidebar">
            <nav class="sidenav shadow-right sidenav-light">
                <div class="sidenav-menu">
                    <div class="nav">
                        <div class="sidenav-menu-heading">Title</div>
                        <a class="nav-link li-sidebar" href="#">Link</a>
                        <a class="nav-link li-sidebar" href="#">Link</a>
                        <a class="nav-link li-sidebar" href="#">Link</a>
                    </div>
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
    border: solid 1px black;
    height: 100vh;
    width: 25rem;
    z-index: 1038;
}
.sidenav{
    background: #662323;
    height: 100%;

}
.li-sidebar{
    color: #FFFFFF;
    font-size: 16px;
    line-height: 20px;
}
</style>