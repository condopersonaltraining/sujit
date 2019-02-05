<template lang="pug">
v-container(grid-list-xs).pa-0
  v-layout(wrap)
    v-flex(v-if="$vuetify.breakpoint.xs" xs12)
      //v-img(:src="require('~/assets/.jpg')" aspect-ratio=2.5)
      v-img(aspect-ratio=2.25).accent
    v-flex(v-else sm4)
      //v-img(:src="require('~/assets/.jpg')" aspect-ratio=1)
      v-img(aspect-ratio=1).accent
    v-flex(xs6 sm4)
      //v-img(:src="require('~/assets/.jpg')" aspect-ratio=1)
      v-img(aspect-ratio=1).accent
    v-flex(xs6 sm4)
      //v-img(:src="require('~/assets/.jpg')" aspect-ratio=1)
      v-img(aspect-ratio=1).accent
  v-container
    v-layout(
      column
      justify-center
      align-center)
      v-flex(
        xs12
        sm8
        md6)
        v-card
          iframe(width="100%" height="250vw" src="https://www.youtube.com/embed/hu1jdqffiOw" frameborder="0" allowfullscreen)
          v-card-title.headline.pb-0 About
          v-card-text.pb-0
            p Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
            p For more information on Vuetify, check out the
              a(
              href="https://vuetifyjs.com"
              target="_blank")
                | link
          transition(name="fade")
            div(v-show="biography")
              v-responsive
                v-img(aspect-ratio=1.75).primary.ma-3
              v-card-title.headline.pb-0 Biography
              v-card-text
                p Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
                p For more information on Vuetify, check out the
                  a(
                  href="https://vuetifyjs.com"
                  target="_blank")
                    | link
          v-card-actions
            v-spacer
            v-btn(primary flat @click="biography = !biography") Read More
        v-card.mt-3
          v-responsive
            v-img.primary(aspect-ratio=1.5)
          v-card-title.headline.pb-0 Previous Work
          v-card-text
            p Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
            p For more information on Vuetify, check out the
              a(
              href="https://vuetifyjs.com"
              target="_blank")
                | link
        v-card.mt-3
          v-responsive
            v-img.primary(aspect-ratio=1.5)
          v-card-title.headline.pb-0 Upcoming Projects
          v-card-text
            p Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
            p For more information on Vuetify, check out the
              a(
              href="https://vuetifyjs.com"
              target="_blank")
                | link

        v-card(flat).accent.mt-3.overflow-x-hidden
          v-card-title.headline.white--text.pb-0 Upcoming Events
          v-container.pr-0
            v-layout.overflow-scroll
              v-card.white.mr-2(min-width="17rem")
                v-card-title
                  h3.title Title
              v-card.white.mr-2(min-width="17rem")
                v-card-title
                  h3.title Title
              v-card.white.mr-2(min-width="17rem")
                v-card-title
                  h3.title Title
              v-card.white(min-width="17rem")
                v-card-title
                  h3.title Title
              v-card.accent.pr-3(flat min-width="0rem")
</template>

<script>

export default {
  data: () => ({
    biography: false
  })
}
</script>

<style>
.v-toolbar__title {
  letter-spacing: 0.2rem
}
.headline {
  letter-spacing: 0.15rem !important
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.overflow-scroll {
  overflow-x: scroll;
}
</style>
