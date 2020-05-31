<template>
  <nav>
    <NavButton
      v-for="section in sections"
      v-bind:key="section"
      :title="section"
      :activeSection="activeSection"
      @button-title="sendBtnTitle"
    />
    <NavButton />
  </nav>
</template>

<script>
import NavButton from "./NavButton.vue";
export default {
  name: "Nav",
  props: ["sections", "activeSection"],
  components: { NavButton },
  methods: {
    sendBtnTitle(btntitle) {
      this.$emit("section-clicked", btntitle);
    }
  }
};
</script>
<style lang="scss">
nav {
  z-index: 1;
  margin: 2 * $unit;
  display: flex;
  justify-content: space-between;
  @media #{$tablet} {
    margin: 2 * $unit 25 * $unit;
  }
  @media #{$desktop} {
    margin: 2 * $unit 45 * $unit;
  }
}
</style>
