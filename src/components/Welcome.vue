<template>
  <section id="welcome" class="hide-overflow">
    <v-layout wrap>
      <v-flex xs12 md6>
        <v-img :src="require('@/assets/profile.jpg')" height="100vh">
          <v-container fill-height text-xs-center>
            <v-layout align-center justify-center>
              <v-flex>
                <span :class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']" class="white--text font-weight-black">
                  <p v-text="schema.basics.name"/>
                </span>
                <span class="white--text font-weight-light" :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']">
                  <p v-text="schema.basics.promo" />
                </span>
              </v-flex>
            </v-layout>
          </v-container>
        </v-img>
      </v-flex>
      <v-flex xs12 md5 :pa-2="$vuetify.breakpoint.smAndDown" wrap>
        <base-bubble-1 style="transform: rotate(180deg) translateY(25%)" />
        <v-layout align-center justify-center>
          <v-flex xs10 md9>
            <base-heading class="info--text">
              Bio
            </base-heading>
            <base-text v-text="schema.basics.bio" />
          </v-flex>
        </v-layout>
        <base-bubble-2 style="transform: rotate(180deg) translate(-200px, -15%)" />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
// Utilities
import { mapState } from 'vuex'

export default {
  name: 'Welcome',
  computed: {
    ...mapState('app', ['schema'])
  }
}
</script>
