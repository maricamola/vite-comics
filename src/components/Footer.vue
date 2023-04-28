<script>
import {mainMenu} from '../data/menus'
import {footerDc} from '../data/menus'
import {footerSites} from '../data/menus'



export default {
  name: 'Footer',
  data(){
    return{
      mainMenu,
      footerDc,
      footerSites
    }
  }
}
</script>

<template>

  <footer>
    <div class="top">
      <div class="colonne">
        <div class="col-column">
        <div class="col">
          <h3>dc comics</h3>
          <nav>
            <ul>
              <li v-for = "(link, index) in mainMenu"
              :key="index">
              <a :class="{'active' : link.isActive}" :href="link.href"> {{ link.text }} </a>
              </li>
            </ul>
          </nav>
        </div>

        <div class="col"><h3>shop</h3>
        <ul>
          <li><a href="#">Shop DC</a></li>
          <li><a href="#">Shop DC Collectibles</a></li>
        </ul></div>
      </div>

      <div class="col">
        <h3> dc </h3>
        <nav>
          <ul>
            <li v-for = "(link, index) in footerDc"
              :key="index">
              <a :href="link.href"> {{ link.text }} </a>
              </li>
          </ul>
        </nav>
      </div>
      <div class="col">
        <h3>sites</h3>
        <nav>
          <ul>
            <li v-for = "(link, index) in footerSites"
              :key="index">
              <a :href="link.href"> {{ link.text }} </a>
              </li>
          </ul>
        </nav>
      </div>


      </div>

      <div class="logo">
        <img src="dc-logo-bg.png" alt="logo-dc">
      </div>
    </div>

    <div class="bottom">
      <div class="container">
        <div class="button">
          <button>SIGN-UP NOW!</button>
        </div>

        <div class="icons">
          <span><h3>FOLLOW US</h3></span>
          <nav>
            <ul>
              <li><a href="#"><img src="footer-facebook.png" alt="logo facebook"></a></li>
              <li><a href="#"><img src="footer-twitter.png" alt="logo twitter"> </a></li>
              <li><a href="#"><img src="footer-youtube.png" alt="logo youtube"></a></li>
              <li><a href="#"><img src="footer-pinterest.png" alt="logo pinterest"></a></li>
              <li><a href="#"><img src="footer-periscope.png" alt="logo periscope"></a></li>
            </ul>
          </nav>
        </div>
      </div>
      
    </div>
  </footer>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/variables' as *;
@use '../scss/general/mixin' as *;

footer{
  background-image: url('../public/footer-bg.jpg');
  background-size: cover;
  .colonne,
  .container {
    @include centerFlex('horizontal');
    width: 80%;
    justify-content: flex-start;
    margin: 0 auto;
    padding: 50px 0;
  }
  .col{
    margin: 20px;
  }
  h3{
    color: white;
    text-transform: uppercase;
  }
  a{
    color: lighten(black, 60%);
    font-size: 12px;
  }
  img{
    width: 700px;
    float: right;
  }
  .top{
    @include centerFlex('horizontal');
    width: 80%;
    margin: 0 auto;
    align-items: center;
    height: 400px;
  }
  .bottom,
  button{
    background-color: #303030;
    position: relative;
  }
  button{
    background-color: none;
    padding: 15px;
    border: 2px solid $primary-color;
    color: white;
    font-weight: bold;
    cursor: pointer;

    &:hover{
      transition: 1s;
      background-color: $primary-color;
    }
  }
  .container{
    @include centerFlex('horizontal');
    justify-content: space-between;
    align-items: center;
    li{
    display: inline-block;
    margin-left: 15px;
  }
  .icons{
    display: flex;
    align-items: center;
  }
  h3{
    color: $primary-color;
    margin: 10px;
  }
  img{
    width: 28px;
  }
  }

}



</style>