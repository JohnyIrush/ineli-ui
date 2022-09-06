<template>
 <div>
     <h2 @mouseover="incrementCount">Hovered {{count}} times</h2>
 </div>
</template>

<script>

//import  CounterMixin from "./CounterTwo";
import { useCounter } from "../../composables/useCounter";

export default {
  name: "HoverCounterTwo",
    //mixins: [CounterMixin],
  watch: {
  },
  setup()
  {
     const {count, incrementCount } = useCounter(100, 10)

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