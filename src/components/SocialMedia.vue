<template>
  <div>
    <contact-dialog v-for="contact in contacts" :key="contact.name" :name="contact.name" :icon="contact.icon" :value="contact.value"></contact-dialog>
  </div>
</template>

<script>
import ContactDialog from './ContactDialog.vue'
export default {
  components: { ContactDialog },
  props: {
    large: {
      type: Boolean,
      default: false
    }
  },

  data: () => ({
    dialog: false,
    contacts: [
      {
        name: 'Facebook',
        icon: 'mdi-facebook',
        value: 'fb/philip.beadle'
      },
      {
        name: 'Email',
        icon: 'mdi-email',
        value: 'me@philt3r.rocks'
      },
      {
        name: 'SMS',
        icon: 'mdi-phone',
        value: '+61 417 301 024'
      }
    ]
  })
}
</script>
