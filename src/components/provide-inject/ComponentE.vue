<template>
 <h2>Component E</h2>
<component-f />
</template>

<script>
import ComponentF from './ComponentF.vue'

export default{
  props: [],
  components:{
    ComponentF
  },
  watch: {
  },
  data () {
    return {
    }
  },
}
</script>

<style scoped>

</style>
