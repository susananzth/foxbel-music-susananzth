<template>
    <div class="navbar fixed-bottom player">
        <div class="container-fluid">
            <p>Player</p>
        </div>
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
.player{
    /* Position */
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: 1039;
    border: solid 1px black;
}
</style>