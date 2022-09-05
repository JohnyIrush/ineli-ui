<template>
  <button @click="showPopup = true">showPopup</button>
  <popup v-show="showPopup" @close="closePopUp" />
</template>

<script>
import Popup from './events/Popup.vue'

export default{
  props: [],
  components:{
    Popup

  },
  watch: {
  },
  data () {
    return {
        showPopup: false
    }
  },
  provide (){
    return {
    }
  },
  methods:{
      closePopUp(name)
      {
          this.showPopup = false
          console.log(name)
      }
  }
}
</script>

<style scoped>

</style>
