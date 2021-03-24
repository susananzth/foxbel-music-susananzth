<template>
    <div id="layoutContent">
        <Sidebar />
        <div id="layoutContent_main">
            <main class="px-5">
                <NavBar />
                <div class="row px-5">
                    <div class="col-12 mb-3">
                        <div class="row">
                        <div class="col-3"><img src="https://source.unsplash.com/TIutDBFEtcY/400x400" class="card-img-top" alt="..."></div>
                        <div class="col-9"></div>
                        </div>
                    </div>
                    <h3 class="text-dark">Resultados</h3>
                    <Card :cover="songs.album.cover" :album="songs.album.title" :title="songs.title" :artist="songs.artist.name" />
                </div>
            </main>
        </div>
    </div>
</template>


<script>
import Sidebar from './Sidebar.vue';
import NavBar from './NavBar.vue';
import Card from "./Card.vue"

export default {
    data(){
        return {
            songs: null,
        };
    },
    name: 'Content',
    components: {
        Sidebar,
        NavBar,
        Card,
    },
    mounted() {
        this.getSongs();
    },
    methods: {
        async getSongs() {
            const res = await fetch("https://api.deezer.com/search/track?q=eminem");
            const data = await res.json();

            this.songs = data;
            console.log(this.songs);
        },
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#layoutContent {
    display: -webkit-box;
    display: flex;
    left: 0;
    right: 0;
    position: fixed;
    top: 0;
}
#layoutContent_main {
    border: solid 1px black;
    top: 3.625rem;
    width: 100%;
}
.btn-primary{
    align-items: center;
    background: #E86060;
    border-radius: 100px;
    color: #FFFFFF;
    display: flex;
    font-size: 14px;
    line-height: 17px;
    mix-blend-mode: normal;
    text-align: center;
}
.btn-primary-border{
    align-items: center;
    border: 1px solid #EB5757;
    border-radius: 100px;
    box-sizing: border-box;
    color: #E86060;
    display: flex;
    font-size: 14px;
    line-height: 17px;
    text-align: center;
}
</style>
