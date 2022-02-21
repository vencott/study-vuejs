<template>
  <!-- $translate 으로 사용 -->
  <h2>{{ $translate("ko.hi") }}</h2>
  <!-- inject로 사용 -->
  <h2>{{ i18n.ko.hi }}</h2>
</template>

<script>
export default {
  inject: ["i18n"],
};
</script>
