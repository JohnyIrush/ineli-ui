<template>
  <h3 v-for="name in names" :key="name">
      <!--{{name.firstname }} {{ name.lastname }}-->
      <slot :firstName="name.firstname" :lastName="name.lastname" ></slot>
  </h3>
</template>

<script>
export default {
name: "NameList",
  data() {
    return {
        names: [
            {
                firstname: 'Bruce',
                lastname: 'Wayne'
            },
            {
                firstname: 'Clark',
                lastname: 'Kent'
            },
            {
                firstname: 'Princess',
                lastname: 'Diana'
            },
            {
                firstname: 'Robert',
                lastname: 'De Niro'
            }
        ]
    }
  },
}
</script>

<style>

</style>