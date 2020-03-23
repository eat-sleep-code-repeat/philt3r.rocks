<template>
  <v-app-bar
      absolute
      color="primary"
      dark
      inverted-scroll
      scroll-target="#recent-sets"
    >
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>
      <SocialMedia />
    </v-app-bar>
</template>

<script>
export default {
  components: {
    SocialMedia: () => import('@/components/SocialMedia')
  }
}
</script>
