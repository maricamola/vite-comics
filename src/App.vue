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

<Header />

<Main />

<Footer />

</template>

<style lang="scss">
//Inserisco gli stili generali che possono essere ereditati da tutta l'app
@use './scss/main'
</style>