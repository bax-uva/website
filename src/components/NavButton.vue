<template>
  <h2
    :class="title == activeSection ? 'active' : 'inactive'"
    @click="sectionClicked"
  >
    {{ title }}
  </h2>
</template>

<script>
export default {
  name: "NavButton",
  props: ["title", "activeSection"],
  methods: {
    sectionClicked() {
      this.$emit("button-title", this.title);
    }
  }
};
</script>
<style lang="scss">
h2 {
  font-weight: lighter;
  cursor: pointer;
}
.active {
  text-decoration: underline;
}
.inactive {
  text-decoration: none;
}
</style>
