<template>
 <div>
     <button @click="incrementCount">Clicked {{count}} times</button>
 </div>
</template>

<script>
import CounterMixin  from "./Counter";
export default {
    name: "ClickCounter",
    mixins: [CounterMixin],
  watch: {
  },
  data()
  {
      return {
          count: 100
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