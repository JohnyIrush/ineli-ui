<template>
  <h3>{{name}}</h3>
</template>

<script>
import { ref } from "vue";
export default {
    name: 'DemoOne',
    setup()
    {
        var name = ref('Vishwas')

        setTimeout(() => {
            name.value = 'Codevolution'
            console.log(name)
        }, 2000);
        
        return {
            name
        }
    }
}
</script>

<style>

</style>