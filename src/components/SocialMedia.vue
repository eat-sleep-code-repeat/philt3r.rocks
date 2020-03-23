<template>
  <div>
    <v-dialog v-model="dialog" v-for="(item, i) in items.slice(0, large ? items.length : 3)" :key="i" :fullscreen="$vuetify.breakpoint.mdAndDown" :hide-overlay="$vuetify.breakpoint.mdAndDown" width="500" transition="dialog-bottom-transition">
      <template v-slot:activator="{ on }">
          <v-btn icon v-on="on" fab class="ma-2" :large="large" color="info">
          <v-icon>{{item.icon}}</v-icon>
          </v-btn>
      </template>
      <v-card>
          <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog = false">
              <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>Contact Details</v-toolbar-title>
          </v-toolbar>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  props: {
    large: {
      type: Boolean,
      default: false
    }
  },  

  data: () => ({
    dialog: false,
    items: [
      {
        name: 'Facebook',
        icon: 'mdi-facebook',
        value: 'https://www.facebook.com/philip.beadle'
      },
      {
        name: 'Email',
        icon: 'mdi-email',
        value: 'me@philt3r.rocks'
      },
      {
        name: 'Phone',
        icon: 'mdi-phone',
        value: '+61 417 301 024'
      }
    ]
  })
}
</script>
