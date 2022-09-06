<template>
  <h3>Options - {{o_name}}</h3>
  <h3>Composition - {{c_name}}</h3>
  <h3>Composition - {{greet}}</h3>
  <h3>Composition - {{c_name}} {{c_lastname}} {{c_heroName}}</h3>
   <h3>Composition - {{greetHero}}</h3>
   <h2>Composition - {{state.firstName}} {{state.lastName}} {{state.heroName}}</h2>
   <h2>Composition - {{reactiveGreetHero}}</h2>
</template>

<script>
import { ref, reactive } from "vue";
export default {
    name: 'Data',
    setup()
    {
       const c_name = ref('Clark')
       const c_lastname = ref('Kent')
       const c_heroName = ref('Superman')

       c_name.value = 'Diana'
       const greet = `Hello ${c_name.value}`
       const greetHero = `Hello ${c_name.value} ${c_lastname.value} a.k.a ${c_heroName.value}`
       console.log(c_name)

       const state = reactive({
           firstName: "princess",
           lastName:'Diana',
           heroName: 'Denzel Washington'
       })

       const reactiveGreetHero =  `Hello ${state.firstName} ${state.lastName}`

       const isLoggedIn = ref(false) 
       const isLoggedInRective = reactive({
          value: false 
       })

       return{
           c_name,
           greet,
           c_lastname,
           c_heroName,
           greetHero,
           state,
           reactiveGreetHero,
           isLoggedIn,
           isLoggedInRective
       }
    },
    data()
    {
        return {
            o_name: "Bruce"
        }
    }
}
</script>

<style>

</style>