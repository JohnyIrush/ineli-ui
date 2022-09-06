<template>
  <!-- Options ---> 
  <input type="text" name="" id="" v-model="name" placeholder="Name">
    <!-- Composition ---> 
  <input type="text" name="" id="" v-model="firstName" placeholder="Composition API Ref First Name">
  <input type="text" name="" id="" v-model="lastName" placeholder="Composition API Ref Last Name">

  <input type="text" name="" id="" v-model="FName" placeholder="Composition API Reactive First Name">
  <input type="text" name="" id="" v-model="LName" placeholder="Composition API Reactive Last Name">
   <input type="text" name="" id="" v-model="options.heroName" placeholder="Composition API Reactive Deep Last Name">
</template>

<script>
import { ref, reactive, toRefs, computed, watch } from "vue";
export default {
    name: "Computed",
    setup()
    {
        
       const firstName = ref('')
       const lastName = ref('Wayne')

       const state = reactive({
           FName: '',
           LName: '',
           options:{
               heroName: ''
           }
       })

/*        watch(()=>{
           return {...state}
       }, function (newValue, oldValue) {
            console.log('fName Old value ', oldValue.FName)
            console.log('fName New value ', newValue.FName)  
            console.log('lName Old value ', oldValue.LName)
            console.log('lName New value ', newValue.LName)  
       }) */

       watch(() => state.options, function(newValue, oldValue) {
            console.log('fName Old value ', oldValue)
            console.log('fName New value ', newValue) 
       },/* {
           immediate: true,
       }, */{
           deep: true
       })

       watch([firstName, lastName], (newValue, oldValue)=>{
            console.log('firstName Old value ', oldValue[0])
            console.log('firstName New value ', newValue[0])  
            console.log('last Name Old value ', oldValue[1])
            console.log('last Name New value ', newValue[1])  
       },/* {
           immediate: true,
       }, */{
           deep: true
       })


       return {
           firstName,
           lastName,
           ...toRefs(state)
       }
    },
    data()
    {
        return{
         name: ''
        }
    },
    watch: {
        name(newValue, oldValue)
        {
            console.log('Old value ', oldValue)
            console.log('New value ', newValue)
        }
    },
  methods: {

  },
}
</script>

<style>

</style>