<template>
  <article class="portfolio-project">
    <h4 class="project-title">
      <a target="_blank" :href="link">{{ title }}</a>
    </h4>
    <p class="project-description">
      {{ description }}
    </p>
    <p class="project-repo" v-show="github">
      <a target="_blank" :href="`https://github.com/bax-uva/${github}`"
        >View project on Github</a
      >
    </p>
    <div class="project-img">
      <img :src="require(`../assets/projects/${image}`)" alt="" />
    </div>
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
  // layout
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, auto);
  column-gap: 2 * $unit;
  row-gap: 1 * $unit;
  margin: 6 * $unit 0 0 0;

  .project-title,
  .project-description,
  .project-repo {
    grid-row-end: span 1;
    grid-column-end: span 2;
    grid-column-start: 1;
  }
  .project-title {
    grid-row-start: 1;
  }
  .project-description {
    grid-row-start: 2;
  }
  .project-repo {
    grid-row-start: 3;
  }
  .project-img {
    grid-row: 1 / span 3;
    grid-column: 3 / span 1;
  }
  img {
    width: 100%;
    height: 100%;
    min-height: 150px;
    max-height: 250px;
    object-fit: cover;
    object-position: center top;
  }

  //   // even projects reversed
  //   :nth-child(even) {
  //     .project-title {
  //       grid-column: 2 / span 2;
  //     }
  //     .project-description {
  //       grid-column: 2 / span 2;
  //     }
  //     .project-repo {
  //       grid-column: 2 / span 2;
  //     }
  //     .project-img {
  //       grid-column: 1 / span 1;
  //     }
  //   }

  @media #{$desktop} {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, auto);
    row-gap: 2 * $unit;
    column-gap: 0;

    .project-title,
    .project-description,
    .project-img,
    .project-repo {
      grid-column: 1 / span 1;
      grid-row-end: span 1;
    }

    .project-title {
      grid-row-start: 1;
    }
    .project-img {
      grid-row-start: 2;
    }
    .project-description {
      grid-row-start: 3;
    }
    .project-repo {
      grid-row-start: 4;
    }

    img {
      min-height: 50px;
      height: 100px;
    }
  }

  // typography
  p {
    font-size: 1.7 * $unit;
    @media #{$desktop} {
      font-size: 2.2 * $unit;
    }
  }
}
</style>
