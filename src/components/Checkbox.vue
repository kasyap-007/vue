<template>
  <div class="container">
    <h1>Vue</h1>
    <form id="form">
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
        v-if="checkList.includes('offset')"
        type="text"
        placeholder="offset"
      />
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
import { store } from '../store.js';
export default {
  name: 'Checkbox',

  data() {
    return {
      store,
      minDate: new Date(Date.now() - 7 * 24 * 60 * 60 * 1000)
        .toISOString()
        .split('T')[0],
      maxDate: new Date().toISOString().split('T')[0],
      checkList: [],
    };
  },
};
</script>

<style>
#form {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.5rem;
  border-radius: 0.25rem;
  --tw-bg-opacity: 1;
  background-color: rgb(255 255 255 / var(--tw-bg-opacity));
  padding: 1rem;
  --tw-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
  --tw-shadow-colored: 0 4px 6px -1px var(--tw-shadow-color),
    0 2px 4px -2px var(--tw-shadow-color);
  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}
</style>
