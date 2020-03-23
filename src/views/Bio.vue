<template>
  <section id="bio">
    <v-row no-gutters>
      <v-col cols="12" md="6">
        <v-img :src="require('@/assets/profile.jpg')" height="100vh" position="start center">
          <v-container fill-height>
            <v-row align="center" class="white--text mx-auto" justify="center">
              <v-col class="white--text text-center" cols="12">
                <span class="font-weight-light" :class="[$vuetify.breakpoint.smAndDown ? 'display-3' : 'display-4']">
                  {{schema.basics.name}}
                </span>
                <br>
                <span :class="[$vuetify.breakpoint.smAndDown ? 'display-1': 'display-2']" class="font-weight-black">
                  {{schema.basics.promo}}
                </span>
              </v-col>
            </v-row>
          </v-container>
        </v-img>
      </v-col>
      <v-col cols="12" md="6">
        <v-row no-gutters>
          <base-bubble-1 style="transform: rotate(180deg) translateY(25%)" />
        </v-row>
        <v-row align="center" justify="center">
          <v-col cols="11">
            <base-heading>
              Bio
            </base-heading>
            <base-text v-text="schema.basics.bio" />
          </v-col>
        </v-row>
        <base-bubble-2 style="transform: rotate(180deg) translate(-200px, -15%)" />
      </v-col>
    </v-row>
  </section>
</template>

<script>
// Utilities
import { mapState } from 'vuex'
export default {
  name: 'Bio',
  computed: {
    ...mapState('app', ['schema'])
  }
}
</script>
