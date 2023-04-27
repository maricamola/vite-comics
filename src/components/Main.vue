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
  background-color: black;
}
.content{
  width: 70%;
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
    margin-left: 60px;
    padding: 20px;
    cursor: pointer;
  }
}

</style>