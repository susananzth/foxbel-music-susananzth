<template>
    <div class="navbar fixed-bottom player">
        <div class="row">
            <div class="col">
                <img class="img-player" src="https://source.unsplash.com/TIutDBFEtcY/400x400" alt="">
                <ul class="d-inline-block align-middle">
                    <li class="bold">Canción</li>
                    <li class="text-small pt-2">Artista - Album</li>
                </ul>
            </div>
            <div class="col-2">
                <div class="multimedia">
                    <button type="button" class="d-inline-block btn btn-back-for"><i class="fas fa-step-backward"></i></button>
                    <button id="play" type="button" class="d-inline-block btn btn-play"><i class="fas fa-play"></i></button>
                    <button type="button" class="d-inline-block btn btn-back-for"><i class="fas fa-step-forward"></i></button>
                </div>
            </div>
            <div class="col">
                <ul class="c-volume">
                    <li class="d-inline-block px-3 py-3"><i class="fas fa-sliders-h volume"></i></li>
                    <li class="d-inline-block px-3 py-3"><i class="fas fa-volume-up volume"></i></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Player',
}
</script>

<style scoped>
.navbar{
    box-shadow: 0 0.15rem 1.75rem 0 rgb(108 108 109 / 48%);
}
.player{
    background: #EB5757;
    bottom: 0;
    color: #fff;
    height: 100px;
    left: 0;
    padding: 0;
    position: fixed;
    right: 0;
    z-index: 1039;
    
}
.row{
    width: 100%;
}
.img-player{
    height: 100px;
    width: 100px;
}
ul {
    list-style-type: none;
    margin-bottom: 0;
}
.text-small{
    font-size: 12px;
}
.multimedia{
    -webkit-box-align: center;
    align-items: center;
    height: 100%;
    -webkit-box-pack: space-evenly;
    justify-content: space-evenly;
    display: -webkit-box;
    display: flex;
    width: 100%;
}
.btn-play{
    background: #FF7676;
    border-radius: 50px;
    color: #fff;
    height: 60px;
    width: 60px;
}
.btn-back-for{
    background: #EB5757;;
    border-radius: 50px;
    color: #fff;
    height: 60px;
    width: 60px;
}
.btn:focus, .btn:hover {
    outline: 0;
    box-shadow: 0 0 0 0.25rem rgb(255 255 255 / 25%);
}
.btn-back-for:focus {
    outline: 0;
    box-shadow: 0 0 0 0.25rem rgb(255 255 255 / 25%);
}
.c-volume{
    -webkit-box-align: center;
    align-items: center;
    height: 100%;
    -webkit-box-pack: flex-end;
    justify-content: flex-end;
    display: -webkit-box;
    display: flex;
    width: 100%;
}
.volume{
    font-size: 36px;
}
</style>