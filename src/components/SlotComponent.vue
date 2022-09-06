<template>
  <name-list >
    <template v-slot:default="slotProps">
      {{slotProps.firstName }} {{ slotProps.lastName }}
    </template>
  </name-list>
</template>

<script>
import NameList from './slots/NameList.vue'
export default {
  components: { NameList },
}
</script>

<style>

</style>