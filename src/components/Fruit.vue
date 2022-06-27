<template>
  <li>{{ name }}</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: "",
    },
  },
};
</script>

<!-- 다른 컴포넌트에 스타일을 미치지 않는다. -->
<style scoped lang="scss">
h1 {
  color: red !important;
}
</style>
