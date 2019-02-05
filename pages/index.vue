<template lang="pug">
  v-layout(
    column
    justify-center
    align-center)
    v-flex(
      xs12
      sm8
      md6)
      v-card
        iframe(width="100%" height="220" src="https://www.youtube.com/embed/hu1jdqffiOw" frameborder="0" allowfullscreen)
        v-card-title.headline.pb-0 About
        v-card-text.pb-0
          p Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
          p For more information on Vuetify, check out the 
            a(
            href="https://vuetifyjs.com"
            target="_blank")
              | link
        div(v-show="background")
          v-responsive
            v-img(aspect-ratio=1.5).primary
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
          v-btn(primary flat @click="background = !background") Read More
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
                      
      v-card(flat dark).mt-3.overflow-x-hidden
        v-card-title.headline.pb-0 Upcoming Events
        v-container(grid-list-md)
          v-layout(wrap)
            v-flex(xs6)
              v-card.white
                v-card-title.black--text Title
            v-flex(xs6)
              v-card.white
                v-card-title.black--text Title
            v-flex(xs6)
              v-card.white
                v-card-title.black--text Title
            v-flex(xs6)
              v-card.white
                v-card-title.black--text Title
</template>

<script>

export default {
  data: () => ({
    background: false
  })
}
</script>

<style>
.v-toolbar__title {
  letter-spacing: 0.2rem
}
.headline {
  letter-spacing: 0.2rem !important
}
</style>
