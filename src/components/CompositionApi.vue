<template>
  <data-component v-if="false"  />
  <methods v-if="false" />
  <v-model v-if="false" />
  <computed v-if="false" />
  <watcher v-if="false" />
  <provide-inject v-if="false" />
  <life-cycle-hooks v-if="false" />
  <template-ref v-if="false" />
  <props v-if="false" />
  <mixin-reusability-two />
</template>

<script>
import Computed from './comosition-api/Computed.vue'
import DataComponent from './comosition-api/Data.vue'
import LifeCycleHooks from './comosition-api/LifeCycleHooks.vue'
import Methods from './comosition-api/Methods.vue'
import ProvideInject from './comosition-api/ProvideInject.vue'
import VModel from './comosition-api/VModel.vue'
import Watcher from './comosition-api/Watcher.vue'
import TemplateRef from './comosition-api/TemplateRef.vue'
import Props from './comosition-api/Props.vue'
import MixinReusabilityTwo from './MixinReusability.vue'
export default {
  components: { DataComponent, Methods, VModel, Computed, Watcher, ProvideInject, LifeCycleHooks, TemplateRef, Props, MixinReusabilityTwo },
}
</script>

<style>

</style>