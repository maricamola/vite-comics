<script>
export default {
  name: 'Header'
}
</script>

<template>
  <header>
    <div class="logo">
    <img src="/dc-logo.png" alt="Logo dc">
  </div>

  <nav>
    <ul>
      <li><a href="#">Characters</a></li>
      <li><a href="#">comics</a></li>
      <li><a href="#">movies</a></li>
      <li><a href="#">tv</a></li>
      <li><a href="#">games</a></li>
      <li><a href="#">collectibles</a></li>
      <li><a href="#">videos</a></li>
      <li><a href="#">fans</a></li>
      <li><a href="#">news</a></li>
      <li><a href="#">shop</a></li>
    </ul>
  </nav>
  </header>
  
</template>
<style lang="scss" scoped>
@use '../scss/general/variables' as *;
@use '../scss/general/mixin' as *;


header{
  @include centerFlex('horizontal');
  color: black;
  padding: 50px;
  align-items: center;
  justify-content: space-between;
  ul{
  @include centerFlex('horizontal');
  margin-bottom: 2rem;
  a{
    display: inline-block;
    text-transform: uppercase;
    margin: 1rem;
    color: black;
  }
}
}

</style>