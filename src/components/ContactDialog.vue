<template>
  <v-dialog v-model="dialog" :fullscreen="$vuetify.breakpoint.mdAndDown" :hide-overlay="$vuetify.breakpoint.mdAndDown" width="500" transition="dialog-bottom-transition">
    <template v-slot:activator="{ on }">
        <v-btn icon v-on="on" fab class="ma-2" :large="large" color="white">
        <v-icon>{{icon}}</v-icon>
      </v-btn>
    </template>
    <v-card class="mx-auto">
      <v-toolbar dark color="primary">
        <v-btn icon dark @click="dialog = false">
            <v-icon>mdi-close</v-icon>
        </v-btn>
        <v-toolbar-title>Contact Details</v-toolbar-title>
      </v-toolbar>
      <v-container fill-height>
        <v-row align="center" class="white--text mx-auto" justify="center">
          <v-col class="white--text text-center" cols="12" tag="h1">
            <span class="font-weight-light" :class="[$vuetify.breakpoint.smAndDown ? 'display-3' : 'display-4']">
              {{name}}
            </span>
            <br>
            <span :class="[$vuetify.breakpoint.smAndDown ? 'display-1': 'display-2']" class="font-weight-black">
              {{value}}
            </span>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  name: 'ContactDialog',
  props: ['large', 'icon', 'name', 'value'],
  data: () => ({
    dialog: false
  })
}
</script>
