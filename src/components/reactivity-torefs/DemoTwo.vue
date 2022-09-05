<template>
  <h3>{{firstname}} {{lastname}}</h3>
</template>

<script>
import { reactive, toRefs } from "vue";
export default {
    name: 'DemoTwo',
    setup()
    {
     
     const state = reactive({
         firstname: "Lil",
         lastname: 'Wayne'
     })

             setTimeout(() => {
            state.firstname = 'Marshal'
            state.lastname = 'Marthers'
            console.log(state)
        }, 2000);

        return toRefs(state)
        /*return {
            state,
            firstname: state.firstname,
            lastname: state.lastname
        }
        */
    },
    data(){
        return {

        }
    }
}
</script>

<style>

</style>