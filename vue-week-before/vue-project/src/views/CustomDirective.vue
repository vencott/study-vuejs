<template>
  <div>
    <div style="height: 1000px">
      <p v-pin="position">페이지 고정 영역</p>
    </div>
  </div>
</template>

<script>
export default {
  directives: {
    pin: {
      mounted(el, binding) {
        el.style.position = "fixed";
        el.style.top = binding.value.top + "px";
        el.style.left = binding.value.left + "px";
      },
    },
  },
  data: function () {
    return {
      position: { top: 50, left: 100 },
    };
  },
};
</script>
