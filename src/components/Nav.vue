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
  width: 80%;
  margin: auto;
  display: flex;
  justify-content: space-between;
  @media #{$tablet} {
    width: 45%;
  }
  @media #{$desktop} {
    width: 40%;
  }
}
</style>
