<template>
  <div id="app">
    <Main />
    <Footer />
  </div>
</template>

<script>
import Footer from './components/macro/Footer.vue'
import Main from './components/macro/Main.vue'


export default {
  name: 'App',
  components: {
    Footer,
    Main  
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';

div {
  font-family: 'PT Sans', sans-serif;
}

</style>
