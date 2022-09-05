<template>
  <data-component v-if="false"  />
  <methods v-if="false" />
  <v-model v-if="false" />
  <computed v-if="false" />
  <watcher />
</template>

<script>
import Computed from './comosition-api/Computed.vue'
import DataComponent from './comosition-api/Data.vue'
import Methods from './comosition-api/Methods.vue'
import VModel from './comosition-api/VModel.vue'
import Watcher from './comosition-api/Watcher.vue'
export default {
  components: { DataComponent, Methods, VModel, Computed, Watcher },
}
</script>

<style>

</style>