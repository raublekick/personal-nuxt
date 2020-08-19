<template>
  <section>
    <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
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
                    type="is-primary has-text-white-bis is-pulled-right"
                    >{{ tag }}</b-tag
                  >
                </b-taglist>
              </div>
            </div>
          </div>
        </div>
      </div>
    </NuxtLink>
  </section>
</template>
<script>
export default {
  props: {
    article: {
      required: true,
      type: Object,
    },
  },
  methods: {
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    },
  },
};
</script>
