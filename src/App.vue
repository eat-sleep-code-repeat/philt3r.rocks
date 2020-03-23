<template>
  <v-app>
    <v-app-bar app absolute color="secondary" dark inverted-scroll scroll-target="#scrolling">
      <v-responsive class="mx-auto">
        <v-row align="center" class="mx-auto" justify="start">
          <v-toolbar-title>{{schema.basics.name}}</v-toolbar-title>
          <v-spacer></v-spacer>
          <social-media/>
        </v-row>
      </v-responsive>
    </v-app-bar>
    <v-sheet id="scrolling" class="overflow-y-auto" max-height="100vh">
      <v-container fluid fill-height>
        <router-view />
      </v-container>
    </v-sheet>
  </v-app>
</template>

<script>
import { mapState } from 'vuex'
export default {
  components: {
    SocialMedia: () => import('@/components/SocialMedia')
  },
  computed: {
    ...mapState('app', ['schema'])
  }
}
</script>
