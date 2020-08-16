<template>
  <footer class="footer">
    <div class="content has-text-white">
      <div class="container">
        <div class="columns">
          <div class="column">
            <blockquote class="has-background-primary has-text-white-ter">
              {{ quote }}
            </blockquote>
          </div>
          <div class="column">
            <div class="columns">
              <div class="column">
                <div class="mb-4">
                  <router-link
                    class="has-text-weight-bold has-text-white-ter"
                    :to="{ name: 'index' }"
                  >
                    Home
                  </router-link>
                </div>
                <div class="mb-4">
                  <router-link
                    class="has-text-weight-bold has-text-white-ter"
                    :to="{ name: 'blog' }"
                  >
                    Blog
                  </router-link>
                </div>
                <div class="mb-4">
                  <router-link
                    class="has-text-weight-bold has-text-white-ter"
                    :to="{ name: 'projects' }"
                  >
                    Projects
                  </router-link>
                </div>
                <div class="mb-4">
                  <router-link
                    type="navbar-item"
                    class="has-text-weight-bold has-text-white-ter"
                    :to="{ name: 'resume' }"
                  >
                    Resume
                  </router-link>
                </div>
              </div>
              <div class="column">
                <div class="mb-4">
                  <a
                    href="mailto:raublekick@gmail.com"
                    target="_blank"
                    class="has-text-white-ter"
                    ><b-icon icon="mail" /> <span>raublekick@gmail.com</span></a
                  >
                </div>
                <div class="mb-4">
                  <a
                    href="https://github.com/raublekick"
                    target="_blank"
                    class="has-text-white-ter"
                    ><b-icon icon="github" /> <span>Git Hub</span></a
                  >
                </div>
                <div class="mb-4">
                  <a
                    href="https://www.linkedin.com/in/jaraub/"
                    target="_blank"
                    class="has-text-white-ter"
                    ><b-icon icon="linkedin" /> <span>LinkedIn</span></a
                  >
                </div>
                <div class="mb-4">
                  <a href="#" target="_blank" class="has-text-white-ter"
                    ><b-icon icon="twitter" /> <span>Twitter</span></a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
import * as _ from "lodash";
export default {
  data() {
    return {
      quotes: [
        "A noble spirit embiggens the smallest man. - Jebediah Springfield",
        "You know what the best currency is and I just thought about this yesterday, the best currency, the most valuable of all, is gratitude. when you’re dead you’re dead, but you’re not quite so dead, if you contribute something. - John Dunsworth",
        "We are all born ignorant, but one must work hard to remain stupid. - Benjamin Franklin",
        "Look your highness, it's not that we're afraid, far from it. It's just that we've got this thing about death; it's not us. - Barf",
      ],
    };
  },
  computed: {
    quote() {
      return this.quotes[_.random(0, this.quotes.length - 1)];
    },
  },
};
</script>
<style scoped>
.footer a {
  display: flex;
}
.footer span {
  margin-left: 0.5em;
}
</style>
