<template>
  <input type="text" name="" id="" :value="modelValue"  @input="$emit('update:modelValue',$event.target.value)" />
</template>

<script>
export default {
    name: "Input",
    props: {
        modelValue: String
    }
}
</script>

<style>

</style>