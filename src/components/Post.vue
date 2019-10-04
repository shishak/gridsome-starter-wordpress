<template>
   <h2 v-html="post.title" />
   <g-link :to="post.path">
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
