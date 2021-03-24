<template>
    <nav class="navbar px-5">
        <div class="container-fluid">
            <form class="col-6 col-xs-9">
                <div class="input-group mb-3">
                    <input type="search" class="form-control input-search" placeholder="Buscar" aria-label="Buscar">
                    <button class="btn btn-search" type="button" id="search"><i class="fas fa-search"></i></button>
                </div>
            </form>
            <a class="d-flex nav-link" href="#!"><i class="fas fa-user nav-link-icon"></i> Francisco M.</a>
        </div>
    </nav>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<style scoped>
.navbar{
    height: 100px;
}
.input-search{
    background: #FFFFFF;
    border: 1px solid #828282;
    border-radius: 100px;
    box-sizing: border-box;
}
.btn-search{
    background: #FFFFFF;
    border: 1px solid #828282;
    border-radius: 100px;
    box-sizing: border-box;
    font-weight: 900;
    font-size: 18px;
    color: #BDBDBD;
    line-height: 21px;
}
.btn-search:active:focus, .btn-search:focus, .input-search:active:focus, .input-search:focus {
    box-shadow: 0 0 0 0.25rem rgb(130 130 130 / 50%);
}
.btn-search:focus {
    box-shadow: 0 0 0 0.25rem rgb(130 130 130 / 50%);
}
.nav-link{
    align-items: center;
    color: #4F4F4F;
    -webkit-box-align: center;
    font-size: 16px;
    line-height: 20px;
    padding-bottom: 0.75rem;
    padding-top: 0.75rem;
    position: relative;
}
.nav-link-icon {
    display: -webkit-inline-box;
    display: inline-flex;
    color: #E86060;
    font-size: 14px;
    margin-right: 0.5rem;
}
</style>