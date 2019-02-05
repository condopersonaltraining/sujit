<template lang="pug">
  v-app
    //v-navigation-drawer(app
      v-model="drawer")
      v-layout(column align-center)
        v-avatar(size=225).mt-4
          v-img(:src="require('~/assets/3065.jpg')" contain)
        h2.headline.mt-3 Sujit Vaidya
        h3.body-1.mt-1 Contemporary Bharatanatyam Artist
      v-container
        
        
    //v-toolbar(
      fixed
      app)
      v-btn(
        icon
        class="primary--text"
        @click.stop="drawer = !drawer")
        v-icon menu
      v-toolbar-title(class="primary--text" v-text="title")
      v-spacer
      v-dialog(v-model="dialog")
        v-btn(class="primary--text text--lighten-1 mr-0" slot="activator" flat) Contact
        v-card
          v-responsive
            v-img(aspect-ratio=2.25).primary
          v-card-title.headline.pb-0 Let's Connect!
          v-card-text.pb-0
            p Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
            v-text-field.pt-1(
              label="Name")
            v-text-field.pt-1(
              label="E-mail")
            v-textarea(
              label="Message").pt-0.pb-0
          v-divider
          v-card-actions
            v-spacer
            v-btn(color="accent") Send
    v-content.secondary
      //v-container(grid-list-xs).pa-0
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
        nuxt
    //v-footer(
      app)
      span.ml-2(color="info") &copy; 2019
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    dialog: false,
    title: 'Bharatanatyam: Vancouver'
  })
}
</script>
