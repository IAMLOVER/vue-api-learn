<template>
  <div>
    <label>
      <input
        v-bind="$attrs"
        :value="value"
        @input="$emit('input', $event.target.value)"
      />
    </label>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: ["label", "value"],
  computed: {
    inputListeners: () => {
      var vm = this;
      return Object.assign({}, this.$listeners, {
        input: () => {
          vm.$emit("input", event.target.value);
        }
      });
    }
  }
};
</script>

<style lang="less" scoped></style>
