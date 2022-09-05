<template>
<custom-input v-model="name" />
</template>

<script >
import CustomInput from './component-v-model/Input.vue'

export default{
  watch: {
  },
  methods: {
  },
  components:{
    CustomInput

  },
  data() {
    return {
        name: ''
    }
  },
  mounted()
  {
    // alert('mounted')
  }
}
</script>

<style scoped>

</style>
