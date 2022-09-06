<template>
 <PropTypesValidation v-show="false" />
 <privide-inject v-if="false" />
 <event v-if="false" />
 <component-vmodel v-if="false" />
 <slot-component v-if="false" />
 <dynamic-component v-if="false" />
 <tele-port v-if="false" />
 <ref v-if="false" />
 <mixin-reusability v-if="false" />
 <composition-api />
 <reactivity-to-refs v-if="false"  />
</template>

<script >
import DynamicComponent from './components/DynamicComponent.vue'
import SlotComponent from './components/SlotComponent.vue'
import ComponentVmodel from './components/ComponentVmodel.vue'
import Event from './components/Event.vue'
import PrivideInject from './components/PrivideInject.vue'
import PropTypesValidation from './components/PropTypesValidation.vue'
import TelePort from './components/TelePort.vue'
import Ref from './components/Ref.vue'
import MixinReusability from './components/MixinReusability.vue'
import CompositionApi from './components/CompositionApi.vue'
import ReactivityToRefs from './components/ReactivityToRefs.vue'

export default{
  watch: {
  },
  methods: {
  },
  components:{
    PropTypesValidation,
    PrivideInject,
    Event,
    ComponentVmodel,
    SlotComponent,
    DynamicComponent,
    TelePort,
    Ref,
    MixinReusability,
    CompositionApi,
    ReactivityToRefs
  },
  data() {
    return {
      greeting: 'Hello World!',
      
    }
  },
  mounted()
  {
    // alert('mounted')
  }
}
</script>

<style scoped>

</style>
