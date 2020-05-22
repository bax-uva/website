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
h1,
h2 {
  font-family: $identity-txt;
  color: $primary-light;
}
a,
a:active,
a:hover {
  color: $link-light;
  text-decoration: none;
}
</style>
