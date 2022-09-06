<template>
 <div>
     <h2 @mouseover="incrementCount">Hovered {{count}} times</h2>
 </div>
</template>

<script>

import  CounterMixin from "./Counter";

export default {
  name: "HoverCounter",
  mixins: [CounterMixin],
  watch: {
  },
  data()
  {
      return {

      }
  },
  methods: {

  },
  created () {
  },
}
</script>

<style>

</style>