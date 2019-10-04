<template>
   <g-link :to="post.path">
   <h2 v-html="post.title" />
   </g-link>  
    <div v-html="post.content" />     
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>
