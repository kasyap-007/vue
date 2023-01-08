<template>
  <h1>Vue</h1>
  <input type="checkbox" id="checkbox" v-model="checked" />
  <label for="checkbox">{{ checked }}</label>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
export default {
  name: 'Checkbox',
  data() {
    return {
      count: 0,
    };
  },
};
</script>
