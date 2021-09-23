<template>
  <section>
    <section class="hero is-medium">
      <div class="hero-body">
        <div class="container">
          <div class="columns is-vcentered">
            <!-- <div class="column has-text-centered">
              <img src="../assets/hero.jpg" />
            </div> -->
            <div class="column has-text-right">
              <h1 class="title">
                (John) Andrew Raub
              </h1>
              <h2 class="subtitle">
                Web Application Developer
              </h2>
              <div>
                <a href="mailto:raublekick@gmail.com" target="_blank"
                  ><b-icon icon="mail" /> <span>raublekick@gmail.com</span></a
                >
              </div>
              <div>
                <a href="https://github.com/raublekick" target="_blank"
                  ><b-icon icon="github" /> <span>Git Hub</span></a
                >
              </div>
              <div>
                <a href="https://www.linkedin.com/in/jaraub/" target="_blank"
                  ><b-icon icon="linkedin" /> <span>LinkedIn</span></a
                >
              </div>
            </div>
            <div class="column">
              <p class="mb-4">
                I am a web application developer specializing in C# / .NET Core,
                MSSQL, Postgres, Vue.js, Nuxt, and more.
              </p>
              <p class="mb-4">
                I have been living in Phoenix, AZ since 2011 and I am heavily
                involved in my local community. I serve on the board of the
                Garfield Organization, a non-profit representing my historic
                neighborhood.
              </p>
              <p>
                Currently I develop web applications for the College of Health
                Solutions at Arizona State University.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="has-background-grey-lighter hero">
      <div class="hero-body">
        <div class="container mb-4">
          <div class="columns">
            <div class="column has-text-centered feature">
              <nuxt-link :to="{ name: 'projects' }">
                <div>
                  <b-icon
                    icon="hammer-wrench"
                    size="is-large"
                    title="Projects"
                  />
                  <p class="title is-4">Projects</p>
                  <p class="subtitle">
                    See what I've been working on in my spare time.
                  </p>
                </div>
              </nuxt-link>
            </div>
            <div class="column has-text-centered feature">
              <nuxt-link :to="{ name: 'community' }">
                <div>
                  <b-icon icon="handshake" size="is-large" title="Community" />
                  <p class="title is-4">Community</p>
                  <p class="subtitle">
                    Projects with my local community.
                  </p>
                </div>
              </nuxt-link>
            </div>
            <!-- <div class="column has-text-centered feature">
              <nuxt-link :to="{ name: 'blog' }">
                <div>
                  <b-icon icon="pencil" size="is-large" title="Blog" />
                  <p class="title is-4">Blog</p>
                  <p class="subtitle">
                    Read about problems and solutions, as well as community
                    engagement topics.
                  </p>
                </div>
              </nuxt-link>
            </div> -->
            <div class="column has-text-centered feature">
              <a
                href="https://registry.jsonresume.org/raublekick"
                title="Resume"
              >
                <div>
                  <b-icon icon="file" size="is-large" title="Resume" />
                  <p class="title is-4">Resume</p>
                  <p class="subtitle">
                    My resume created with jsonresume.org.
                  </p>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  name: "HomePage",
};
</script>
