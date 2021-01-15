<template>
  <div id="app">
    <router-view></router-view>
    <footer-guide></footer-guide>
  </div>
</template>

<script>
import FooterGuide from './components/FooterGuide/FooterGuide.vue'
export default {
 components:{
   FooterGuide
 }
}
</script>

<style lang='stylus'>
#app
  width 100%
  height 100%
</style>
