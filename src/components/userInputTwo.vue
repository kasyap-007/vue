<template>
  <div class="container">
    <div class="header">
      <h1>User Input Two</h1>
      <form id="form" @submit.prevent="submit">
        <label for="partition2">
          <input
            value="partition2"
            type="checkbox"
            v-model="checkList"
            name="partition2"
            id="partition2"
          />
          Partition
        </label>
        <input
          v-if="checkList.includes('partition2')"
          type="text"
          placeholder="partition"
          v-model="partition2"
        />
        <label for="offset2">
          <input
            value="offset2"
            type="checkbox"
            v-model="checkList"
            name="offset2"
            id="offset2"
          />
          Offset
        </label>
        <input
          v-model="offset2"
          v-if="checkList.includes('offset2')"
          type="text"
          placeholder="offset"
        />
        <button type="submit">Submit</button>
      </form>
    </div>
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
      partition2: '',
      offset2: '',

      checkList: [],
      userData: '',
    };
  },
  methods: {
    submit() {
      var data = {
        partition: this.partition2,
        offset: this.offset2,
      };
      this.userData = data;
    },
  },
};
</script>
