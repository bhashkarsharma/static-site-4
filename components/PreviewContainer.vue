<template lang="pug">
div.preview-container
  h2.preview-title(v-if="title")  {{ title }}
  div.preview-content
    slot
  nuxt-link.see-all(v-if="seeAll" :to="seeAll.path") {{ seeAll.label }}
</template>

<script>
export default {
  props: {
    title: { type: String },
    seeAll: { type: Object }
  }
}
</script>

<style lang="sass">
@import "../assets/sass/util"


.preview-container
  max-width: $w-preview
  min-height: 24rem
.preview-content
  margin-top: 1rem
  margin-bottom: -1rem
  li
    padding-bottom: .5rem

.see-all
  font-size: 1.25rem
  opacity: .8
</style>
