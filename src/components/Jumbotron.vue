<script>
export default {
  name: 'Jumbotron' 
}
</script>


<template>
  <div class='jumbotron'></div>
</template>


<style lang="scss" scoped>
@use '../scss/general/variables' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/utility' as *;

.jumbotron{
    height: 400px;
    background-image: url(../public/jumbotron.jpg);
    background-size: cover;
  }


</style>