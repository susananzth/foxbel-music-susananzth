<template>
  <Player />
  <Content />
</template>

<script>
import Player  from './components/Player.vue';
import Content from './components/Content.vue';


export default {
  name: 'App',
  components: {
    Player,
    Content,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Quicksand&display=swap');
* {
  font-family: 'Quicksand', sans-serif;
  font-style: normal;
  font-weight: normal;
}
h1, h2, h3, h4, h5, h6{
  font-weight: bold;
  font-size: 22px;
  line-height: 27px;
  color: #FFFFFF;
}
</style>
