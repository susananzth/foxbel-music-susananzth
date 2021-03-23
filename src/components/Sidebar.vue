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

<script>
export default {
  name: 'Player',
  props: {
    msg: String
  }
}
</script>

<style scoped>
#layoutSidebar {
    width: 15rem;
    height: 100vh;
    z-index: 1038;
    border: solid 1px black;
}
.sidebar{
  background: #662323;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
}
.li-sidebar{
  font-size: 16px;
  line-height: 20px;
  color: #FFFFFF;
}
</style>