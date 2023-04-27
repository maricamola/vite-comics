<script>
import {mainMenu} from '../data/menus'

export default {
  name: 'Header',
  data(){
    return{
      mainMenu
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
      <li v-for = "(link, index) in mainMenu"
      :key="index">
      <a :class="{'active' : link.isActive}" :href="link.href"> {{ link.text }} </a>
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
    font-weight: bold;
    &:hover{
      color: #0282F9;
    }
  }
}
}

</style>