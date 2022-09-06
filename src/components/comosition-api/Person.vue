<template>
<input type="text" name="" id="" placeholder="First Name" v-model="firstName" />
<input type="text" name="" id="" placeholder="Last Name" v-model="lastName" />
 <greeting :firstName="firstName" :lastName="lastName" @callHeroes="callHeroes" />
</template>

<script>
import { ref, reactive, toRefs, computed, watch, onMounted } from "vue";
import Greeting from './Greeting.vue';

export default {
  components: { Greeting },
    name: "Person",
    setup()
    {
      const firstName = ref('')
      const lastName = ref('')

        function callHeroes(hero)
        {
            alert(hero)
        }

       return {
         firstName,
         lastName,
         callHeroes
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