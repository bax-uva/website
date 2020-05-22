<template>
  <article class="portfolio-project">
    <div class="project-txt">
      <h4><a href="#">Project title</a></h4>
      <p>
        Project description Lorem ipsum dolor sit amet, consectetur adipisicing
        elit. Dolores alias enim veritatis debitis corporis omnis perspiciatis
        delectus facere aut dolores ipsam.
      </p>
      <p><a href="#">View project on Github</a></p>
    </div>
    <img src="https://via.placeholder.com/150" alt="" />
  </article>
</template>

<script>
export default {
  name: "Project"
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
