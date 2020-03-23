<template>
  <section id="releases" class="hide-overflow">
    <v-layout>
      <v-flex xs12 md6 pa-5>
        <v-layout align-center justify-center fill-height wrap>
          <v-flex xs12>
            <base-bubble-2 style="transform: translateX(55%)" />
            <base-heading>
              Releases
            </base-heading>
          </v-flex>
          <v-flex v-for="(release, i) in schema.releases" :key="i" md6 text-xs-center mb-3>
            <iframe width="100%" :height="iframeHeight" :src="release.src" frameborder="0"></iframe>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex hidden-sm-and-down md6>
        <v-img :src="require('@/assets/releases.jpg')" height="100%" />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'Releases',
  computed: {
    ...mapState('app', ['schema']),
    iframeHeight () {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs': return '320'
        case 'sm': return '350  '
        case 'md': return '450'
        case 'lg': return '420'
        case 'xl': return '500'
      }
      return '1000'
    }
  }
}
</script>
