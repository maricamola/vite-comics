<script>
export default {
  name: 'ProductCard',
  props:{
    image: String,
    productName: String
  }
}
</script>

<template>
  <div class="cards">
    <img :src="image" :alt="productName">
    <h4>{{ productName }}</h4>
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/general/variables' as *;

.cards{
  text-align: center;
  img{
    width: 80px;
    height: 80px;
    margin: 30px;
  }
  h4{
    color: white;
    font-size: 12px;
    font-weight: lighter;
  }
}

</style>