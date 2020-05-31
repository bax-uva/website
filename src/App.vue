<template>
  <div id="app">
    <Background />
    <Header />
    <Nav
      :sections="sections"
      :activeSection="activeSection"
      @section-clicked="updateSection"
    />
    <About :activeSection="activeSection" v-show="activeSection == 'about'" />
    <Work
      :projects="projects"
      :activeSection="activeSection"
      v-show="activeSection == 'work'"
    />
    <Contact
      :activeSection="activeSection"
      v-show="activeSection == 'contact'"
    />
  </div>
</template>

<script>
import projects from "./data/data.json";
import Background from "./components/Background.vue";
import Header from "./components/Header.vue";
import Nav from "./components/Nav.vue";
import About from "./components/About.vue";
import Work from "./components/Work.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
    Background,
    Header,
    Nav,
    About,
    Work,
    Contact
  },
  data: () => {
    return {
      projects,
      sections: ["about", "work", "contact"],
      activeSection: " "
    };
  },
  methods: {
    updateSection(section) {
      this.activeSection = section;
    }
  }
};
</script>

<style lang="scss">
html,
body {
  padding: 0;
  margin: 0;
  background: $background-dark;
  color: $text-light;
  font-family: $body-txt;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app {
  display: flex;
  flex-direction: column;
}
h1,
h2 {
  font-family: $identity-txt;
  color: $primary-light;
}
h1,
h2,
h3,
h4 {
  margin: 0;
  line-height: 100%;
  font-weight: lighter;
}
h1 {
  font-size: 2.6 * $unit;
  @media #{$desktop} {
    font-size: 3 * $unit;
  }
}
h2 {
  font-size: 4.6 * $unit;
  @media #{$mobileM} {
    font-size: 5.4 * $unit;
  }
  @media #{$mobileL} {
    font-size: 6.3 * $unit;
  }
  @media #{$tablet} {
    font-size: 5.6 * $unit;
  }
  @media #{$desktop} {
    font-size: 6.5 * $unit;
  }
}

h4 {
  font-size: 2.5 * $unit;
}
p {
  font-kerning: auto;
  margin: 0;
  font-size: 2 * $unit;
  line-height: 150%;
  @media #{$tablet} {
    text-align: justify;
    font-size: 2.3 * $unit;
  }
  @media #{$desktop} {
    font-size: 2.5 * $unit;
    line-height: 160%;
    text-align: justify;
  }
}
a,
a:active {
  color: $link-light;
  text-decoration: none;
  &:hover {
    text-decoration: underline;
  }
}
section {
  z-index: 1;
  margin: 3 * $unit auto;
  margin: 3 * $unit;
  @media #{$tablet} {
    margin: 2 * $unit 25 * $unit 20 * $unit 25 * $unit;
  }
  @media #{$desktop} {
    margin: 2 * $unit 45 * $unit 20 * $unit 45 * $unit;
  }
}
</style>
