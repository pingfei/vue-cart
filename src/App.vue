<template>
  <div id="app">
    <h1>Vue 组件设计与实践</h1>
    <!-- <img src="./assets/logo.png"> -->
    <!-- <div>
      <p>
        If Element is successfully added to this project, you'll see an
        <code v-text="'<el-button>'"></code>
        below
      </p>
      <el-button>el-button</el-button>
    </div> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <from-test></from-test>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import FromTest from './components/FormTest'
export default {
  name: 'app',
  components: {
    // HelloWorld,
    FromTest
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
