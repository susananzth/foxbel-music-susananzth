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
                            <div class="col-9">a</div>
                        </div>
                    </div>
                    <h3 class="text-dark">Resultados</h3>
                    <div class="col-2 py-2" v-for="song in songs" :key="song.id">
                        <div class="card">
                            <i class="fas fa-ellipsis-v btn-option"></i>
                            <i class="fas fa-play card-btn-play"></i>
                            <img :src="song.picture" class="card-img-top" alt=" album }}">
                            <div class="card-body ">
                                <p class="card-title">{{ song.title }}</p>
                                <p class="card-text">{{ song.user.name }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </div>
</template>


<script>
import Sidebar from './Sidebar.vue';
import NavBar from './NavBar.vue';
import axios from 'axios';

export default {
    name: 'Content',
    components: {
        Sidebar,
        NavBar,
    },
    data(){
        return{
            songs:[]
        }
    },
    mounted(){
        this.getSongs();
    },
    methods: {
        getSongs(){
            axios.get('https://api.deezer.com/search/playlist?q=top')
                .then( response => {
                    this.songs = response.data.data;
                })
                .catch( e => console.log(e));
        }
    },
};
</script>

<style scoped>
#layoutContent {
    display: -webkit-box;
    display: flex;
    left: 0;
    right: 0;
    top: 0;
}
#layoutContent_main {
    padding-bottom: 120px;
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

/* card */
.card {
    border: none;
    border-radius: 0;
}
.card-img-top {
    border-top-left-radius: 0;
    border-top-right-radius: 0;
}
.card-body {
    padding: .2rem .1rem;
}
.card-title{
    font-size: 14px;
    font-weight: bold;
    margin-bottom: 0;
}
.card-text{
    font-size: 12px;
}
.card-btn-play{
    color: #fff;
    font-size: 36px;
    position: absolute;
    right: 40%;
    text-shadow: 2px 0px 5px rgba(150, 150, 150, 1);
    top: 35%;
}
.btn-option{
    color: #fff;
    float: right;
    position: absolute;
    right: 2%;
    text-shadow: 2px 0px 5px rgba(150, 150, 150, 1);
    top: 2%;
}
</style>
