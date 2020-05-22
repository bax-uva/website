<template>
  <section class="work">
    <p>
      I’ve been working with Lorem ipsum dolor sit amet, consectetur adipisicing
      elit. Animi corporis, culpa nesciunt. Numquam debitis nihil eos architecto
      delectus nisi repellendus soluta laborum distinctio reprehenderit totam
      assumenda, voluptatum, incidunt ipsum natus!
    </p>
    <div class="projects-wrapper">
      <Project /> <Project /><Project /> <Project />
    </div>
  </section>
</template>

<script>
import Project from "./Project.vue";
export default {
  name: "Work",
  components: {
    Project
  }
};
</script>
<style lang="scss">
.projects-wrapper {
  margin-top: 4 * $unit;
}
</style>
