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
