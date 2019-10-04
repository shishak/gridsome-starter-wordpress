<template>
   <g-link :to="post.path">
    <div v-html="post.excerpt" />
    <h2 v-html="post.title" />
   </g-link>     
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
