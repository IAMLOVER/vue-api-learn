<template>
  <div>
    <span>
      <slot :user="user">
        {{ user.lastName }}
      </slot>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        lastName: "lastName",
        firstName: "firstName"
      }
    };
  }
};
</script>

<style lang="less"></style>
