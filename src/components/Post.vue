<template>
   <g-link :to="post.path" class="grid-item">
    <div v-html="post.content" />
    <div class="gradient"><h2 v-html="post.title" /></div>
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
