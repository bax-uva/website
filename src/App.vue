<template>
  <div id="app">
    <Header />
    <Nav />
    <About />
    <Work />
    <Contact />
  </div>
</template>

<script>
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
}
h1 {
  font-size: 3 * $unit;
}
h2 {
  font-size: 5 * $unit;
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
a:active,
a:hover {
  color: $link-light;
  text-decoration: none;
}
section {
  width: 80%;
  margin: 2 * $unit auto;
}
</style>
