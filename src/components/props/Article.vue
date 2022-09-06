<template>
  <div :id="id" class="">
   <h1>Article component</h1>
   <h2 v-bind="$attrs">Title - {{title}}</h2>
   <h2>Likes = {{likes}}</h2>
   <h2>Published = {{(isPublished)? 'Yes': 'No'}}</h2>
   <h2>Author = {{Author}}</h2>
  </div>
</template>

<script >
export default{
  name: 'Article',
  props: {
    title: String,
    likes: Number,
    isPublished: Boolean,
    Author:{
      type: String,
      required: true,
      default: 'vince gilligan'
    },
    id: String
  },
  inheritAttrs: false,
  components:{

  }
}
</script>

<style scoped>

</style>
