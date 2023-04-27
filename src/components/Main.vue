<script>
export default {
  name: 'Main'
}
</script>
<template>
  <main>
    <div class='content'>
      <h1> Content goes here </h1>
    </div>

    <div class="loghi">
      <ul>
        
      </ul>
    </div>
  </main>

</template>
<style lang="scss" scoped>
@use '../scss/general/variables' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/utility' as *;

.content{
  background-color: #1C1C1C;
  h1{
    color: white;
    padding: 70px 50px;
  }
}

.loghi{
  background-color: $primary-color;
}

</style>