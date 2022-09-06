<template>
 <person />
</template>

<script>
import { ref, reactive, toRefs, computed, watch, onMounted } from "vue";
import Person from './Person.vue';

export default {
  components: { Person },
    name: "TemplateRef",
    setup()
    {

       return {
       }
    },
    data()
    {
        return{

        }
    },
  methods: {

  },
  mounted()
  {

  }
}
</script>

<style>

</style>