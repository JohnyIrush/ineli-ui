<template>
 <h3>Child Component B</h3>
 <child-c />
</template>

<script>
import { ref, reactive, toRefs, computed, watch } from "vue";
import ChildC from './ChildC.vue';
export default {
  components: { ChildC },
    name: "ChildB",
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