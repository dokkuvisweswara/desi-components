<template>
  <div id="app">
    <btn :label="LOGIN" @myclick="myclick"></btn>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import btn from  "./components/Button.vue"
export default {
  name: 'App',
  methods: {
    myclick () {
      alert(1)
    }
  },
  components: {
    btn
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
  margin-top: 60px;
}
</style>
