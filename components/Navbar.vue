<template>
  <b-navbar class="has-shadow is-spaced" wrapper-class="container">
    <template slot="brand">
      <b-navbar-item tag="router-link" :to="{ name: 'index' }">
        <img :src="require('../assets/hero.jpg')" /> (John) Andrew Raub
      </b-navbar-item>
    </template>
    <template slot="start"> </template>

    <template slot="end">
      <b-navbar-item tag="a" href="mailto:raublekick@gmail.com">
        <b-icon icon="mail" />
      </b-navbar-item>
      <b-navbar-item tag="a" href="https://github.com/raublekick">
        <b-icon icon="github" />
      </b-navbar-item>
      <b-navbar-item tag="a" href="https://www.linkedin.com/in/jaraub/">
        <b-icon icon="linkedin" />
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ name: 'index' }">
        Home
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ name: 'blog' }">
        Blog
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ name: 'projects' }">
        Projects
      </b-navbar-item>
      <b-navbar-item
        tag="router-link"
        type="navbar-item"
        :to="{ name: 'resume' }"
      >
        Resume
      </b-navbar-item>
    </template>
  </b-navbar>
</template>
<script>
export default {
  name: "Navbar",
  data() {
    return {};
  },
};
</script>

<style>
.navigation-bar {
  z-index: 10;
}
.navigation-bar.shadow {
  box-shadow: 0px 0px 4px #666;
}
</style>
