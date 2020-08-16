<template>
  <div>
    <navbar />

    <section class="">
      <!-- <aside class="column is-2 section">
        <p class="menu-label is-hidden-touch">
          General
        </p>
        <ul class="menu-list">
          <li v-for="(item, key) of items" :key="key">
            <nuxt-link :to="item.to" exact-active-class="is-active">
              <b-icon :icon="item.icon" /> {{ item.title }}
            </nuxt-link>
          </li>
        </ul>
      </aside> -->

      <!-- <div class="container column is-10"> -->
      <nuxt />
      <!-- </div> -->
    </section>

    <nav-footer />
  </div>
</template>

<script>
import Navbar from "../components/Navbar";
import NavFooter from "../components/NavFooter";

export default {
  components: {
    Navbar,
    NavFooter,
  },
  data() {
    return {
      items: [
        {
          title: "Home",
          icon: "home",
          to: { name: "index" },
        },
        {
          title: "Blog",
          icon: "lightbulb",
          to: { name: "blog" },
        },
        {
          title: "Projects",
          icon: "pencil",
          to: { name: "projects" },
        },
        {
          title: "Resume",
          icon: "file",
          to: { name: "resume" },
        },
      ],
    };
  },
};
</script>
