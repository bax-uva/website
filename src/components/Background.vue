<template>
  <div class="background">
    <div
      v-for="particle in 15"
      :class="`particle p${particle}`"
      :key="particle"
      :style="{
        top: Math.random() * (800 - -50) + -50 + 'px',
        left: Math.random() * (1540 - 50) + -50 + 'px'
        /* transform: 'translate(' + 50 + '%)' */
      }"
    ></div>
  </div>
</template>
<script>
export default {
  name: "Background"
};
</script>
<style>
.background {
  background: black;
  width: 100%;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
}
.particle {
  top: 0;
  left: 0;
  width: 70px;
  height: 130px;
  background-image: linear-gradient(
    to top,
    rgba(16, 100, 39, 0),
    rgba(16, 100, 39, 0.4)
  );
  position: fixed;
  transform: rotate(-10deg);
  border-radius: 2px;
}
</style>
