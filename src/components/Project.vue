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
    <img src="../assets/projects/baianaPB.png" alt="" />
  </article>
</template>

<script>
export default {
  name: "Project",
  props: ["title", "link", "description", "github", "image"]
};
</script>
<style lang="scss">
article {
  display: flex;
  justify-content: space-between;
  margin: 6 * $unit 0 0 0;

  @media #{$desktop} {
    flex-direction: column;
  }
  .project-txt {
    width: 55%;

    @media #{$desktop} {
      width: 100%;
    }
  }

  p {
    font-size: 1.7 * $unit;
    margin: 2 * $unit 0 0 0;

    @media #{$desktop} {
      font-size: 1.9 * $unit;
    }
  }

  img {
    width: 40%;
    height: auto;
    object-fit: cover;
    object-position: center top;
    @media #{$desktop} {
      width: 100%;
    }
  }
  &:nth-child(even) {
    flex-direction: row-reverse;
    @media #{$desktop} {
      flex-direction: column;
    }
  }
}
</style>
