<template>
  <div class="container">
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less">
.container {
  width: 500px;
  height: 500px;
  background-color: red;
  color: #000;
}
</style>
