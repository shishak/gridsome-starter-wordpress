<template>
   <g-link :to="post.path">
    <h2 v-html="post.title" />
    <div v-html="post.content" />
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
