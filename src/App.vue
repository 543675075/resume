<template>
  <div id="app">
      <nav-bar></nav-bar>
      <vue-full-page></vue-full-page>
  </div>
</template>

<script>
  import VueFullPage from './components/content/fullpage/fullpage.vue'
  import NavBar from './components/content/navbar.vue'
  export default {
    name: 'App',
    components: {
      VueFullPage,
      NavBar
    }
  }
</script>

<style lang="less">
 
</style>