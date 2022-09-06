<template>
 <div>
     <button @click="incrementCount">Clicked {{count}} times</button>
 </div>
</template>

<script>
//import CounterMixin  from "./Counter";
import { useCounter } from "../../composables/useCounter";
export default {
    name: "ClickCounterTwo",
    //mixins: [CounterMixin],
  watch: {
  },
  setup()
  {
     const {count, incrementCount } = useCounter()

     return{
         count,
         incrementCount
     }
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