<template>
  <nav>
    <NavButton />
    <NavButton />
    <NavButton />
  </nav>
</template>

<script>
import NavButton from "./NavButton.vue";
export default {
  name: "Nav",
  components: { NavButton }
};
</script>
<style lang="scss">
nav {
  width: 80%;
  margin: auto;
  display: flex;
  justify-content: space-between;
}
</style>
