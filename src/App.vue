<template>
  <div id="app">
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
import Header from "./components/Header.vue";
import Nav from "./components/Nav.vue";
import About from "./components/About.vue";
import Work from "./components/Work.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
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
}
h2 {
  font-size: 4 * $unit;
}
button {
  background: white;
}
h4 {
  font-size: 2.5 * $unit;
}
p {
  margin: 0;
  font-size: 2 * $unit;
  line-height: 140%;
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
  width: 80%;
  margin: 4 * $unit auto;
}
</style>
