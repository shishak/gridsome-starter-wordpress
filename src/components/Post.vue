<template>
   <g-link :to="post.path">
    <div v-html="post.content" class="grid-item" />
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
