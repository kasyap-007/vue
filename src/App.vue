<template>
  <div id="app">
    <userInputOne />
    <userInputTwo />
  </div>
</template>

<script>
import userInputOne from './components/userInputOne.vue';
import userInputTwo from './components/userInputTwo.vue';
import './styles.css';
export default {
  name: 'App',
  components: {
    userInputOne,
    userInputTwo,
  },
};
</script>
