<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components:{
      Header,
      Main,
      Footer
  }
}
</script>

<template>

  <header />

  <main />

  <footer />
  
</template>

<style lang="scss">
.container{
  h1{
    background-color:cadetblue;
  }
}
</style>