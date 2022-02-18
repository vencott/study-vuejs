<template>
  <div>
    <child-component @send-message="sendMessage" ref="child_component" />
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent4.vue";
export default {
  components: { ChildComponent },
  methods: {
    sendMessage(data) {
      console.log(data);
    },
  },
};
</script>
