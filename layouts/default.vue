<template lang="pug">
  v-app
    v-navigation-drawer(
      app
      right="true"
      v-model="drawer")
      v-layout
    v-toolbar(
      fixed
      app)
      v-toolbar-title(class="primary--text" v-text="title")
      v-spacer
      v-btn(v-if="!drawer" @click.stop="drawer = !drawer" class="primary--text text--lighten-1 mr-0" flat) Contact
      //v-dialog(v-model="dialog")
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
    title: 'Sujit Vaidya'
  })
}
</script>
