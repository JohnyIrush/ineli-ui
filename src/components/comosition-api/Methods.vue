<template>
  {{name}}
  <button @click="setName">Change Name</button>

  <h2>{{count}}</h2>
  <button @click="incrementCount">Increment Count</button>
</template>

<script>
import { ref, reactive, toRefs } from "vue";
export default {
  watch: {
  },
    name: "Methods",
    setup()
    {
       const count = ref(0)
       const state = reactive({
         firstname: "Lil",
         lastname: 'Wayne'
       })

       function incrementCount() {
           count.value++
       }

       return {
           count,
           incrementCount,
           ...toRefs(state)
       }
    },
    data()
    {
        return{
            name: 'Vishwas'
        }
    },
  methods: {
      setName()
      {
          this.name = "Codevolution"
      }
  },
}
</script>

<style>

</style>