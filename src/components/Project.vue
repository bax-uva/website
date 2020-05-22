<template>
  <article class="portfolio-project">
    <div class="project-txt">
      <h4>
        <a :href="link">{{ title }}</a>
      </h4>
      <p>
        {{ description }}
      </p>
      <p v-show="github">
        <a :href="`https://github.com/bax-uva/${github}`"
          >View project on Github</a
        >
      </p>
    </div>
    <img src="https://via.placeholder.com/150" alt="" />
  </article>
</template>

<script>
export default {
  name: "Project",
  props: ["title", "link", "description", "github"]
};
</script>
<style lang="scss">
article {
  display: flex;
  justify-content: space-between;
  margin: 6 * $unit 0 0 0;

  .project-txt {
    width: 65%;
  }

  p {
    font-size: 1.7 * $unit;
    margin: 2 * $unit 0 0 0;
  }

  img {
    width: 30%;
  }
  &:nth-child(even) {
    flex-direction: row-reverse;
  }
}
</style>
