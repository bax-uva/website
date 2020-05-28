<template>
  <header>
    <h1>bax uva</h1>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>
<style lang="scss">
header {
  z-index: 1;
  display: flex;
  height: 16 * $unit;
  @media #{$tablet} {
    height: 22 * $unit;
  }
  @media #{$desktop} {
    height: 24 * $unit;
  }
  h1 {
    margin: 2 * $unit 0 0 2 * $unit;
  }
}
</style>
