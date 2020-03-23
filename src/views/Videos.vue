<template>
  <section id="videos" class="hide-overflow">
    <v-layout>
      <v-flex hidden-sm-and-down md6>
        <v-img :src="require('@/assets/videos.jpg')" height="100%" />
      </v-flex>
      <v-flex xs12 md6 pa-5>
        <v-layout align-center justify-center fill-height wrap>
          <v-flex xs12>
            <base-bubble-2 style="transform: translateX(55%)" />
            <base-heading>
              Videos
            </base-heading>
          </v-flex>
          <v-flex v-for="(video, i) in schema.videos" :key="i" xs12 text-xs-center mb-3>
            <div class="container">
              <iframe :src="video" frameborder="0" allowfullscreen class="video"></iframe>
            </div>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'Videos',
  computed: {
    ...mapState('app', ['schema'])
  }
}
</script>

<style lang="sass">
.container
  position: relative
  width: 100%
  height: 0
  padding-bottom: 56.25%

.video
  position: absolute
  top: 0
  left: 0
  width: 100%
  height: 100%

</style>
