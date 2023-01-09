<template>
  <div class="container">
    <div class="header">
      <h1>User Input One</h1>
      <form id="form" @submit.prevent="submit">
        <label for="partyid">
          <input
            type="checkbox"
            v-model="checkList"
            name="partyid"
            value="partyid"
            id="partyid"
          />
          Party ID
        </label>
        <input
          v-if="checkList.includes('partyid')"
          type="text"
          placeholder="party id"
          v-model="partyid"
        />
        <label for="corelation">
          <input
            type="checkbox"
            v-model="checkList"
            value="corelation"
            name="corelation"
            id="corelation"
          />
          corelation ID
        </label>
        <input
          v-model="corelation"
          v-if="checkList.includes('corelation')"
          type="text"
          placeholder="corelation"
        />
        <label for="date">
          <input
            value="date"
            type="checkbox"
            v-model="checkList"
            name="date"
            id="date"
          />
          Date
        </label>
        <input
          v-model="date"
          v-if="checkList.includes('date')"
          type="date"
          name=""
          id=""
          :max="maxDate"
          :min="minDate"
        />
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
    </div>
    <pre class="output">
    <span>Output</span>
    {{ userData }}
  </pre
    >
  </div>
</template>

<script>
export default {
  name: 'userInputOne',

  data() {
    return {
      partyid: '',
      corelation: '',
      date: '',
      partition: '',
      offset: '',
      minDate: new Date(Date.now() - 7 * 24 * 60 * 60 * 1000)
        .toISOString()
        .split('T')[0],
      maxDate: new Date().toISOString().split('T')[0],
      checkList: [],
      userData: '',
    };
  },
  methods: {
    submit() {
      var data = {
        partyid: this.partyid,
        corelation: this.corelation,
        date: this.date,
        partition: this.partition,
        offset: this.offset,
      };
      this.userData = data;
    },
  },
};
</script>
