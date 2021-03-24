<template>
    <div class="col-2 py-2">
        <div class="card">
            <i class="fas fa-ellipsis-v btn-option"></i>
            <i class="fas fa-play btn-play"></i>
            <img src="{{ cover }}" class="card-img-top" alt="{{ album }}">
            <div class="card-body ">
                <p class="card-title">{{ title }}</p>
                <p class="card-text">{{ artist }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        cover: String,
        album: String,
        title: String,
        artist: String,
    },
}
</script>

<style>
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
.btn-play{
    color: #fff;
    font-size: 36px;
    position: absolute;
    right: 50%;
    text-shadow: 2px 0px 5px rgba(150, 150, 150, 1);
    top: 50%;
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