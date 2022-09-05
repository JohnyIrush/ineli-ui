<template>
 <div class="">
   <h2>This is a popup</h2>
   <input type="text" name="" id="" v-model="name">
   <button  @click="$emit('close',name)">Close Popup</button>
 </div>
</template>

<script>

export default{
  props: [],
  emits: {
    close: (name) =>{
      if (!name) {
        return false
      }else{
        return true
      }
    }
  },
  components:{

  },
  watch: {
  },
  data () {
    return {
      name: ''
    }
  },
  provide (){
    return {
        
    }
  },
}
</script>

<style scoped>

</style>
