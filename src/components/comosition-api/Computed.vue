<template>
  <input type="text" name="" id="" v-model="firstname" placeholder="first name">
  <input type="text" name="" id="" v-model="lastname" placeholder="last name">
  Options - {{fullName}}
  
 <input type="text" name="" id="" v-model="refFirstName" placeholder="Composition ref first name">
  <input type="text" name="" id="" v-model="refLastName" placeholder="Composition ref last name">
  Composition ref - {{refFullname}}

   <input type="text" name="" id="" v-model="reactivefirstname" placeholder="Composition reactive first name">
  <input type="text" name="" id="" v-model="reactivelastname" placeholder="Composition reactive last name">
  Composition reactive - {{reactivefullname}}
</template>

<script>
import { ref, reactive, toRefs, computed } from "vue";
export default {
  watch: {
  },
    name: "Computed",
    setup()
    {
        
       const refFirstName = ref('')
       const refLastName = ref('')

      const refFullname = computed(function() {
           return `${refFirstName.value} ${refLastName.value}`
       })

       const state = reactive({
         reactivefirstname: "",
         reactivelastname: ''
       })

      const reactivefullname = computed(function() {
           return `${state.reactivefirstname} ${state.reactivelastname}`
       })

       return {
           refFirstName,
           refLastName,
           refFullname,
           ...toRefs(state),
           reactivefullname
       }
    },
    computed:{
        fullName()
        {
            return this.firstname + ' ' + this.lastname
        }
    },
    data()
    {
        return{
         firstname: "",
         lastname: ''
        }
    },
  methods: {
      setName()
      {
          this.name = "Codevolution"
      }
  },
}
</script>

<style>

</style>