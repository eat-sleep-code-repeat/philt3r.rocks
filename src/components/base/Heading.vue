<template>
  <component
    :is="tag"
    :class="[$vuetify.breakpoint.smAndDown ? 'display-2': 'display-3']" 
    class="v-heading mb-3 font-weight-light"
  >
    <slot />
  </component>
</template>

<script>
export default {
  props: {
    tag: {
      type: String,
      default: 'h1'
    }
  }
}
</script>

<style lang="sass">
  .v-heading
    letter-spacing: 3px !important
</style>
