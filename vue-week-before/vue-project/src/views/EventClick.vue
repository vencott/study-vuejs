<template>
  <div>
    <button type="button" @click="increaseCounter">Add</button>
    <p>The counter is : {{ counter }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increaseCounter: function () {
      this.counter += 1;
    },
  },
};
</script>
