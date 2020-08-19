<template>
  <section class="section container">
    <article>
      <div class="columns">
        <div class="column is-one-fifth has-text-right"></div>
        <div class="column has-background-white-ter blog-body">
          <h1 class="title has-text-primary">{{ article.title }}</h1>
          <h2 class="subtitle">{{ article.description }}</h2>

          <b-taglist>
            <b-tag
              v-for="tag in article.tags"
              :key="tag"
              type="is-primary has-text-white-bis"
              ><NuxtLink
                class="has-text-white-bis"
                :to="{ name: 'blog-tag-tag', params: { tag: tag } }"
                >{{ tag }}</NuxtLink
              ></b-tag
            >
          </b-taglist>
          <time :datetime="article.createdAt">{{
            formatDate(article.createdAt)
          }}</time>

          <nuxt-content :document="article" />
        </div>
        <div class="column is-one-fifth">
          <div v-if="article.toc" class="blog-menu sticky">
            <h5 class="subtitle is-uppercase">Contents</h5>

            <ul>
              <li
                v-for="link of article.toc"
                :key="link.id"
                :class="{
                  toc2: link.depth === 2,
                  toc3: link.depth === 3,
                }"
              >
                <NuxtLink :to="`#${link.id}`">{{ link.text }}</NuxtLink>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </article>
  </section>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content("articles", params.slug).fetch();

    return { article };
  },
  methods: {
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    },
  },
};
</script>
<style></style>
