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
  width: calc(80% / 6);
  text-align: center;
  margin: 10px;
  text-align: center;
  cursor: pointer;
  img{
    width: 100%;
    height: 200px;
    object-fit: contain;
    margin-top: 50px;
    &:hover{
      transition: 1s;
      filter: brightness(50%);
    }
  }
  h4{
    color: white;
    font-size: 14px;
    font-weight: lighter;
    word-wrap: break-word;
    margin-top: 10px;
  }
}

</style>