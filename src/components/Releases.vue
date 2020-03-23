<template>
  <section
    id="releases"
    class="hide-overflow"
  >
    <v-layout white>
      <v-flex
        xs12
        md6
        pa-5
      >
        <base-bubble-1 style="transform: translate(5%, -5%)" />
        <base-heading class="info--text">
          Releases
        </base-heading>
        <v-card>
          <v-container
            grid-list-md
            pa-2
          >
            <v-layout wrap>
              <v-flex
                v-for="(release, i) in schema.releases"
                :key="i"
              >
                <iframe width="100%" :height="iframeWidth" :src="release.src" frameborder="0"></iframe>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
      <v-flex
          hidden-sm-and-down
          md6
        >
          <v-img
            :src="require('@/assets/releases.jpg')"
            height="100%"
          />
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
    iframeWidth () {
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
