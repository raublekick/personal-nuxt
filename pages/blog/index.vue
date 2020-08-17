<template>
  <section class="section container">
    <h1 class="title has-text-primary">Blog Posts</h1>
    <ul>
      <li v-for="article of articles" :key="article.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
          <div class="card">
            <div class="card-content">
              <div class="media">
                <div class="media-content">
                  <p class="title is-4">{{ article.title }}</p>
                  <!-- <p class="subtitle is-6">@johnsmith</p> -->
                </div>
              </div>

              <div class="content">
                {{ article.description }}
                <!-- <a href="#">#css</a> <a href="#">#responsive</a> -->
                <br />
                {{ article.tags }}
                <time :datetime="article.createdAt">{{
                  formatDate(article.createdAt)
                }}</time>
              </div>
            </div>
          </div>
        </NuxtLink>
      </li>
    </ul>
  </section>
</template>
<script>
export default {
  async asyncData({ $content, params }) {
    const articles = await $content("articles", params.slug)
      .only(["title", "description", "img", "slug", "createdAt", "tags"])
      .sortBy("createdAt", "asc")
      .fetch();

    return {
      articles,
    };
  },
  methods: {
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    },
  },
};
</script>
