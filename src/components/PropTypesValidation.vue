<template>
<Article :id="'myArticle'" :title="'Article Title'" :likes="50" :isPublished="true" />
</template>

<script >
import Article from "./props/Article.vue";
export default{
  watch: {
  },
  data () {
    return {
    }
  },
  props: [],
  components:{
    Article
  }
}
</script>

<style scoped>

</style>
