<template>
  <div id="app">
    <div id="parent">
      <userInputOne />
      <userInputTwo />
    </div>
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
