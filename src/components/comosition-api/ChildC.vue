<template>
 <h3>Child Component B</h3>
<h3>Options username {{userName}}</h3> 
<h3>Composition username {{childUserName}}</h3> 

 <h3>Child Component count {{ childCount }}</h3>
 <h3>Child Component hero {{ firstName  }} {{ lastName  }}</h3>
 <button @click="incrementCount">increment child count</button>
</template>

<script>
import { ref, reactive, toRefs, computed, watch, inject } from "vue";
export default {
    name: "ChildC",
    setup()
    {

     const childUserName = inject('c_name',"SoftwaresCares")
     const childCount = inject('c_count',10)
     const childHero = inject('c_hero',{})
     const incrementCount = inject('incrementCount')

       return {
         childUserName,
         childCount,
         ...toRefs(childHero),
         incrementCount
       }
    },
    inject: ['userName'],
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