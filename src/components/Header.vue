<script>
import {mainMenu} from '../data/menus'

export default {
  name: 'Header',
  data(){
    return{
      mainMenu,
      counter: 0
    }
  }
}
</script>

<template>
  <header>
    <div class="logo">
    <img src="/dc-logo.png" alt="Logo dc">
  </div>

  <nav>
    <ul>
      <li v-for = "(menu, index) in mainMenu"
      :key="index">
      <a :class="{'active' : counter == index}" @click="counter = index" :href="menu.href"> {{ menu.text }} </a>
      </li>
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
  align-items: self-end;
  justify-content: space-between;
  width: 80%;
  margin: 0 auto;
  padding-top: 5px;
  img{
    width: 80%;
  }
  ul{
  @include centerFlex('horizontal');
  a{
    display: inline-block;
    text-transform: uppercase;
    margin: 0 10px;
    color: #464646;
    font-weight: bold;
    font-size: 14px;
    padding-bottom: 30px;
    &:hover{
      color: #0282F9;
    }
    &:active{
      border-bottom: 3px solid #0282F9;
    }
  }
  .active{
    border-bottom: 3px solid #0282F9;
  }
}
}

</style>