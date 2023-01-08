<template>
  <h1>Vue</h1>
  <label for="checkbox">
    Checkbox
    <input type="checkbox" id="checkbox" v-model="checked" />
  </label>
  {{ checked ? 'hi' : '' }}
  <input type="date" v-if="checked" />

  <!-- <button @click="count++">Count is: {{ count }}</button> -->
</template>

<script>
export default {
  name: 'Checkbox',

  data() {
    return {
      // count: 0,
      checked: true,
    };
  },
};
</script>
