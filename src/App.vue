<template>
  <div id="app">
    <HeaderNavbar />
    <div id='content' class="content">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import HeaderNavbar from './components/layout/Header'

export default {
  name: 'App',
  components: {
    HeaderNavbar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#content {
  margin-top: 1em;
  }
</style>
