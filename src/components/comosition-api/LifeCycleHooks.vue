<template>
 <button id="count" @click="count++">clicked {{ count }}</button>
</template>

<script>
import { ref, reactive, toRefs, computed, watch, provide, onMounted, onUpdated, onUnmounted } from "vue";

export default {
    name: "ProvideInject",
    setup()
    {
        var count = ref(0)

        let intervalId

        onMounted(() => {
            console.log("onMounted LifeCycle")
          intervalId += setInterval(() => {
            return 10
          }, 1000)

        })

        onUpdated(() => {
            console.log("onUpdate LifeCycle")
        })
        

        onUnmounted(
            () =>{
                 clearInterval(intervalId,3000)
                 console.log("onUnmounted LifeCycle")
            }
            )

       return {
           count
          }
    },
    data()
    {
        return{
        }
    },

  methods: {

  },
}
</script>

<style>

</style>