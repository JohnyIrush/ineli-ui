<template>
  <tab-wrapper>
      <tab title="Tab One">Hello From Tab 1</tab>
      <tab title="Tab Two">Hello From Tab 2</tab>
      <tab title="Tab Three">Hello From Tab 3</tab>
      <tab title="Tab Four">Hello From Tab 4</tab>
  </tab-wrapper>
</template>

<script>
import Tab from './Tab.vue'
import TabWrapper from './TabWrapper.vue'
export default {
  components: { TabWrapper, Tab },

}
</script>

<style>

</style>