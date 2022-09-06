<template>
<h3>ProvideInject Component username {{name}}</h3>
<component-c />
</template>

<script>
import ComponentC from './provide-inject/ComponentC.vue'

export default{
  props: [],
  components:{
     ComponentC
  },
  watch: {
  },
  data () {
    return {
      name: 'Johnte'
    }
  },
  provide (){
    return {
      username: this.name 
    }
  },
}
</script>

<style scoped>

</style>
