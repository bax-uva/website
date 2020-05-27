<template>
  <section class="work">
    <p>
      I’ve been working with Lorem ipsum dolor sit amet, consectetur adipisicing
      elit. Animi corporis, culpa nesciunt. Numquam debitis nihil eos architecto
      delectus nisi repellendus soluta laborum distinctio reprehenderit totam
      assumenda, voluptatum, incidunt ipsum natus!
    </p>
    <div class="projects-wrapper">
      <Project
        v-for="project in projects"
        v-bind:key="project.title"
        :title="project.title"
        :link="project.link"
        :description="project.description"
        :github="project.githubRepo"
      />
    </div>
  </section>
</template>

<script>
import Project from "./Project.vue";
export default {
  name: "Work",
  props: ["projects"],
  components: {
    Project
  }
};
</script>
<style lang="scss">
.work {
  .projects-wrapper {
    margin-top: 4 * $unit;
  }
}
</style>
