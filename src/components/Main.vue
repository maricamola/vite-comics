<script>
import ProductCard from './ProductCard.vue'
import products from '../data/products'

export default {
  name: 'Main',
  data() {
    return {
      products
    }
  },
  components:{
    ProductCard
  }
}

</script>

<template>
  <main>
    <div class="container">

    <ProductCard 
      v-for="(product, index) in products"
      :key="index"
      :image="product.thumb"
      :productName="product.series"
    />

    </div>

    <button>
      LOAD MORE
    </button>
    

    <div class="loghi">
      <ul>
        <li><img src="buy-comics-digital-comics.png" alt="digital comics"> digital comics </li>
        <li><img src="buy-comics-merchandise.png" alt="merchandise">dc merchandise</li>
        <li><img src="buy-comics-subscriptions.png" alt="subscriptions">subscriptions</li>
        <li><img src="buy-comics-shop-locator.png" alt="comic shop locator">comic shop locator</li>
        <li><img src="buy-dc-power-visa.svg" alt="power visa">dc power visa</li>
      </ul>
    </div>
  </main>

</template>
<style lang="scss" scoped>
@use '../scss/general/variables' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/utility' as *;

main{
  background-color: #1C1C1C;
  text-align: center;
  .container{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 80%;
  }
  button{
    color: white;
    font-size: 12px;
    font-weight: bold;
    margin: 20px;
    padding: 10px 20px;
    background-color: $primary-color;
    border: none;
    cursor: pointer;
    &:hover{
      background-color:lighten($primary-color, 10%);
    }
  }
}
.content{
  width: 80%;
  margin: 0 auto;
  h1{
    color: white;
    padding: 70px 0px;
  }
}

.loghi{
  @include centerFlex('horizontal');
  background-color: $primary-color;
  text-transform: uppercase;
  color: white;
  font-size: 12px;
  img{
    width: 40px;
    vertical-align: middle;
    margin: 10px;
    cursor: pointer;
  }
  ul{
    @include centerFlex('horizontal');
    align-items: center;
  }
  li{
    display: inline-block;
    padding: 20px;
    margin: 0 20px;
    cursor: pointer;
    &:hover{
      transition: 1s;
      font-size: 14px;
    }
  }
}

</style>