<template>
  <div>
    <p>{{ title }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: String
  },
  created() {
    this.$emit("update:title", "子组件的title");
  }
};
</script>

<style lang="less" scoped></style>
