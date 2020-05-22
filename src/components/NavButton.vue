<template>
  <h2>
    {{ title }}
  </h2>
</template>

<script>
export default {
  name: "NavButton",
  props: ["title", "activeSection"],
  data: () => {
    return {
      isActive: false
    };
  },
  methods: {
    updateSection() {}
  }
};
</script>
<style lang="scss"></style>
