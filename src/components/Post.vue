<template>
   <g-link :to="post.path" class="grid-item">
    <div v-html="post.content" />
    <span :to="post.date" />
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
