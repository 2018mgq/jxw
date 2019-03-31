<template>
  <div id="app">
    <router-view></router-view>
     <Tabber/>
  </div>
</template>
<script>
import Tabber from './common/tabber'
export default {
  components:{
    Tabber
  }
}
</script>

<style>
  #app{
    display:flex;

  }
</style>
