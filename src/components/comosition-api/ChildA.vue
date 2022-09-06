<template>
 <h3>Child Component A</h3>
 <child-b />
</template>

<script>
import { ref, reactive, toRefs, computed, watch } from "vue";
import ChildB from './ChildB.vue';
export default {
  components: { ChildB },
    name: "ChildA",
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