<template>
 <h3>Parent Component {{ name }}</h3>
 <child-a />
</template>

<script>
import { ref, reactive, toRefs, computed, watch } from "vue";
export default {
    name: "ProvideInject",
    setup()
    {
        


       return {

       }
    },
    data()
    {
        return{
         name: ''
        }
    },
  methods: {

  },
}
</script>

<style>

</style>