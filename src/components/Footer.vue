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
        <img src="/dc-logo-gb.png" alt="logo-dc">
      </div>
      
    </div>

    <div class="bottom">

    </div>
  </footer>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/variables' as *;
@use '../scss/general/mixin' as *;

footer{
  background-image: url('../public/footer-bg.jpg');
  .colonne{
    @include centerFlex('horizontal');
    width: 70%;
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
    z-index: 99;
  }
  .top{
    @include centerFlex('horizontal');
  }
}

</style>