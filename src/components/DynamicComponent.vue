<template>
<button @click="activeTab = 'TabA'">Tab A</button>
<button @click="activeTab = 'TabB'">Tab B</button>
<button @click="activeTab = 'TabC'">Tab C</button>
  <!--<tab-a v-if="activeTab === 'TabA'" />
  <tab-b v-if="activeTab === 'TabB'" />
  <tab-c v-if="activeTab === 'TabC'" />-->

  <keep-alive>
      <component :is="activeTab"></component>
  </keep-alive>
</template>

<script>
import TabA from './dynamic-components/TabA.vue'
import TabB from './dynamic-components/TabB.vue'
import TabC from './dynamic-components/TabC.vue'
export default {
  components: { TabA, TabB, TabC },
  data() {
    return {
        activeTab: 'TabA'
    }
  },
}
</script>

<style>

</style>