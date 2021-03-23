<template>
    <div id="layoutContent">
        <Sidebar />
        <div id="layoutContent_main">
            <main>
              <p>Content</p>
            </main>
        </div>
    </div>
</template>


<script>
import Sidebar from '../components/Sidebar.vue';

export default {
  name: 'Content',
  components: {
        Sidebar,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#layoutContent {
    display: -webkit-box;
    display: flex;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
}

#layoutContent_main {
    top: 3.625rem;
    border: solid 1px black;
}
.btn-search{
  background: #FFFFFF;
  border: 1px solid #828282;
  box-sizing: border-box;
  border-radius: 100px;
}
.btn-primary{
  background: #E86060;
  mix-blend-mode: normal;
  border-radius: 100px;
  font-size: 14px;
  line-height: 17px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #FFFFFF;
  mix-blend-mode: normal;
}
.btn-primary-border{
  border: 1px solid #EB5757;
  box-sizing: border-box;
  border-radius: 100px;
  font-size: 14px;
  line-height: 17px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #E86060;
}
</style>
