<template>
  <click-counter />
  <hover-counter />
</template>

<script>
import ClickCounter from './mixins/ClickCounter.vue'
import HoverCounter from './mixins/HoverCounter.vue'

export default {
  components: { ClickCounter, HoverCounter },
  watch: {
  },
  methods: {
  },
  created () {
  },

}
</script>

<style>

</style>