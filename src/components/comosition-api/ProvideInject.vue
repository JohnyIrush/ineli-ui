<template>
 <h3>Parent Component {{ name }}</h3>
 <h3>Parent Component count {{ count }}</h3>
 <h3>Parent Component hero {{ firstName  }} {{ lastName  }}</h3>
 <button @click="incrementCount">increment parent count</button>
 <child-a />
</template>

<script>
import { ref, reactive, toRefs, computed, watch, provide } from "vue";
import ChildA from './ChildA.vue';
export default {
  components: { ChildA },
    name: "ProvideInject",
    setup()
    {

      provide('c_name', 'Codevolution')

      const count = ref(0)

      function incrementCount()
      {
        count.value++
      }
      const state = reactive({
        firstName: "Bruce",
        lastName: "Wayne"
      })      
      

         provide('c_count', count)
         provide('c_hero', state)
         provide('incrementCount', incrementCount)

       return {
         count,
         ...toRefs(state),
         incrementCount
       }
    },
    data()
    {
        return{
         name: 'vishwas'
        }
    },
    provide()
    {
      return {
        userName: this.name,
      }
    },
  methods: {

  },
}
</script>

<style>

</style>