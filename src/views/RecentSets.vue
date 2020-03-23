<template>
  <v-sheet id="recent-sets" class="hide-overflow">
    <v-layout>
      <v-flex xs12 md6 pa-5>
        <v-layout align-center justify-center fill-height wrap>
          <v-flex xs12>
            <base-bubble-2 style="transform: translateX(55%)" />
            <base-heading>
              Recent Sets
            </base-heading>
          </v-flex>
          <v-flex v-for="(mix, i) in schema.mixes" :key="i" md6 text-xs-center mb-3>
             <iframe width="100%" height="200" :src="mix" frameborder="0"></iframe>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex hidden-sm-and-down md6>
        <v-img :src="require('@/assets/recent-sets.jpg')" height="100%" />
      </v-flex>
    </v-layout>
  </v-sheet>
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
