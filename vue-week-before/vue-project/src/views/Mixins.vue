<template>
  <div>
    <div>{{ htmlString }}</div>
    <div v-html="htmlString"></div>
  </div>
</template>

<script>
import ApiMixin from "../api.js";

export default {
  mixins: [ApiMixin],
  data() {
    return {
      productList: [],
    };
  },
  async mounted() {
    this.productList = await this.$callAPI(
      "https://3d5348c0-4158-4724-ad6f-352e7ef79ceb.mock.pstmn.io/list",
      "get"
    );
    console.log(this.productList);
  },
};
</script>
