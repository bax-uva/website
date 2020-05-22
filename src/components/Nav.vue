<template>
  <nav>
    <NavButton
      v-for="section in sections"
      v-bind:key="section"
      :title="section"
      :activeSection="activeSection"
    />
    <NavButton />
  </nav>
</template>

<script>
import NavButton from "./NavButton.vue";
export default {
  name: "Nav",
  props: ["sections", "activeSection"],
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
