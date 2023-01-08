<template>
  <div class="container">
    <h1>User Input Two</h1>
    <form id="form" @submit.prevent="submit">
      <label for="partition">
        <input
          value="partition"
          type="checkbox"
          v-model="checkList"
          name="partition"
          id="partition"
        />
        Partition
      </label>
      <input
        v-if="checkList.includes('partition')"
        type="text"
        placeholder="partition"
        v-model="partition"
      />
      <label for="offset">
        <input
          value="offset"
          type="checkbox"
          v-model="checkList"
          name="offset"
          id="offset"
        />
        Offset
      </label>
      <input
        v-model="offset"
        v-if="checkList.includes('offset')"
        type="text"
        placeholder="offset"
      />
      <button type="submit">Submit</button>
    </form>
    <pre class="output">
    {{ userData }}
  </pre
    >
  </div>
</template>

<script>
export default {
  name: 'userInputTwo',

  data() {
    return {
      partition: '',
      offset: '',

      checkList: [],
      userData: '',
    };
  },
  methods: {
    submit() {
      var data = {
        partition: this.partition,
        offset: this.offset,
      };
      this.userData = data;
    },
  },
};
</script>
