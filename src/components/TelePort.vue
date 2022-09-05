<template>
<teleport to="#portal-root">
    <portal />
</teleport>
</template>

<script>
import Portal from './teleport/Portal.vue'
export default {
  components: { Portal },

}
</script>

<style>

</style>