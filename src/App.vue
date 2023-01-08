<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Checkbox />
  </div>
</template>

<script>
import Checkbox from './components/Checkbox.vue';

export default {
  name: 'App',
  components: {
    Checkbox,
  },
};
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
