<template>
  <div id="app">
    <Header title="Shop"></Header>
    <!--<img alt="Vue logo" src="./assets/logo.png">-->
  </div>
</template>

<script>
import Header from './components/Header.vue'
import News from './components/News.vue'

export default {
  name: 'App',
  components: {
    Header,
    News
  }
}
</script>

<style lang="less">
* {
  margin: 0;
  padding: 0;
}

/*#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
</style>
