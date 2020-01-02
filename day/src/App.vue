<template>
  <div id="app">
    <div class="main">
      <router-view/>
    </div>
    <Footer />
  </div>
</template>
<script>
import Footer from './components/Footer'
export default {
  components: {
    Footer
  }
}
</script>
<style lang="scss">
@import url('./assets/css/reset.scss');
#app {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  .main{
    flex: 1;
    width: 100%;
    display: flex;
    flex-direction: column; 
    overflow: auto;
  }
  .footer{
    width: 100%;
    height: 40px;
    display: flex;
  }
}
</style>
