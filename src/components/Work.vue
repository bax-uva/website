<template>
  <section class="work">
    <p>
      Here is a sample of my open-source work and side projects.
    </p>
    <div class="projects-wrapper">
      <Project
        v-for="project in projects"
        v-bind:key="project.title"
        :title="project.title"
        :link="project.link"
        :description="project.description"
        :github="project.githubRepo"
        :image="project.image"
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
