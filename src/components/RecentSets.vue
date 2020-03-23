<template>
  <section
    id="recent-projects"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        xs12
        md6
        primary
        pa-5
        white--text
      >
        <base-bubble-1 style="transform: rotate(180deg) translateX(25%)" />
        <base-heading>
          Recent Sets
        </base-heading>
        <v-card color="secondary">
          <v-container
            grid-list-md
            pa-2
          >
            <v-layout wrap>
              <v-flex
                v-for="mix in schema.mixes"
                :key="mix"
              >
                <iframe width="100%" height="200" :src="mix" frameborder="0"></iframe>
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
          :src="require('@/assets/recent-sets.jpg')"
          height="100%"
        />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'RecentSets',
  computed: {
    ...mapState('app', ['schema'])
  }
}
</script>
