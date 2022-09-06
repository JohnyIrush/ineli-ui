<template>
  <input type="text" name="" id="" ref="inputRef" />
</template>

<script>
import { ref, reactive, toRefs, computed, watch, onMounted } from "vue";

export default {
    name: "TemplateRef",
    setup()
    {
        const inputRef = ref(null)

        onMounted(()=>{
           inputRef.value.focus()
        })

       return {
           inputRef
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
      alert('1')
      //this.$refs.inputRef.focus()   
  }
}
</script>

<style>

</style>