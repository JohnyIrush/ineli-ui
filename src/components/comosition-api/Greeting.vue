<template>
<div>Hello {{ fullName }}  </div>
<button @click="sendEvent">Call Heroes</button>
</template>

<script>
import { ref, reactive, toRefs, computed, watch, onMounted } from "vue";

export default {
    name: "Greeting",
    props: ["firstName", "lastName"],
    setup(props, context)
    {
        const fullName = computed(() =>{
            return `${props.firstName} ${props.lastName}`
        })

        function sendEvent()
        {
            context.emit("callHeroes",fullName.value)
        }

       return {
           fullName,
           sendEvent
       }
    },
    emits: ["callHeroes"],
 /*    computed:{
        fullName (){
            return `${this.firstName} ${this.lastName}`
        }
    }, */
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