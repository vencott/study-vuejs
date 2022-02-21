<template>
  <div>
    <h2>Calculator</h2>
    <div>
      <!-- 키이벤트 삭제 -->
      <input type="text" v-model="num1" />
      <span> + </span>
      <input type="text" v-model="num2" />
      <span> = </span>
      <span>{{ result }}</span>
    </div>
  </div>
</template>

<script>
import { reactive, computed } from "vue"; // computed 추가
export default {
  name: "calculator",
  setup() {
    let state = reactive({
      num1: 0,
      num2: 0,
      // computed를 이용해서 num1, num2가 변경이 일어나면 즉시 result로 더한 값을 반환
      result: computed(() => parseInt(state.num1) + parseInt(state.num2)),
    });
    return {
      state,
    };
  },
};
</script>
