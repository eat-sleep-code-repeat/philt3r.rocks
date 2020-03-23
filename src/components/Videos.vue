<template>
  <section
    id="videos"
    class="hide-overflow"
  >
    <v-layout accent>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/videos.jpg')"
          height="100%"
        />
      </v-flex>
      <v-flex
        xs12
        md6
        pa-5
      >
        <v-layout
          align-center
          justify-center
          fill-height
          wrap
        >
          <v-flex xs12>
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="info--text">
              Videos
            </base-heading>
          </v-flex>
          <v-flex
            v-for="(video, i) in schema.videos"
            :key="i"
            md6
            text-xs-center
            mb-3
          >
             <iframe width="100%" height="400" :src="video" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
