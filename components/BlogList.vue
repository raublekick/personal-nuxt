<template>
  <section class="articles">
    <div class="columns is-centered">
      <div class="column is-three-fifths">
        <div v-for="article of articles" :key="article.slug">
          <blog-item :article="article" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import BlogItem from "./BlogItem";

export default {
  components: {
    BlogItem,
  },
  props: {
    articles: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>
