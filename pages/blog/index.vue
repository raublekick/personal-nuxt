<template>
  <section class="section container">
    <h1 class="title has-text-primary">Blog Posts</h1>
    <section class="articles">
      <div class="columns is-centered">
        <div class="column is-three-fifths">
          <div v-for="article of articles" :key="article.slug">
            <NuxtLink
              :to="{ name: 'blog-slug', params: { slug: article.slug } }"
            >
              <div class="card article">
                <div class="card-content">
                  <div class="content">
                    <div class="columns">
                      <div class="column is-one-fifth has-text-right">
                        <time :datetime="article.createdAt">{{
                          formatDate(article.createdAt)
                        }}</time>
                      </div>
                      <div class="column">
                        <p class="title is-4">{{ article.title }}</p>
                        <p class="subtitle is-6">{{ article.description }}</p>
                        <b-taglist>
                          <b-tag
                            v-for="tag in article.tags"
                            :key="tag"
                            type="is-primary has-text-white is-pulled-right"
                            >{{ tag }}</b-tag
                          >
                        </b-taglist>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </NuxtLink>
          </div>
        </div>
      </div>
    </section>
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
