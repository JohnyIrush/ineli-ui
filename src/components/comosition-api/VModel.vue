<template>
  <input type="text" name="" id="" v-model="fname" placeholder="first name">
  <input type="text" name="" id="" v-model="lname" placeholder="last name">

  <input type="text" name="" id="" v-model="heroname" placeholder="hero name">
  <input type="text" name="" id="" v-model="firstname" placeholder="first name">
  <input type="text" name="" id="" v-model="lastname" placeholder="last name">
</template>

<script>

import { ref, reactive, toRefs } from "vue";
export default {
    setup()
    {
       const heroname = ref('')

       const state = reactive({
         firstname: "",
         lastname: ''
       })


       return {
           heroname,
           ...(state)
       }
    },
    data()
    {
        return{
         fname: "",
         lname: ''
        }
    },
}
</script>

<style>

</style>