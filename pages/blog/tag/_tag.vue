<template>
  <section class="section container">
    <h1 class="title has-text-primary">
      Blog Posts
      <b-tag type="is-primary has-text-white-bis is-large">{{
        $route.params.tag
      }}</b-tag>
    </h1>
    <blog-list :articles="articles" />
  </section>
</template>
<script>
import BlogList from "../../../components/BlogList";

export default {
  components: {
    BlogList,
  },
  async asyncData({ $content, params }) {
    const articles = await $content("articles", params.slug)
      .only(["title", "description", "img", "slug", "createdAt", "tags"])
      .where({ tags: { $contains: params.tag } })
      .sortBy("createdAt", "asc")
      .fetch();

    return {
      articles,
    };
  },
};
</script>
