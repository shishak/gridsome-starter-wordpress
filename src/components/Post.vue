<template>
   <g-link :to="post.path" class="grid-item">
    <div v-html="post.content" />
    <h2 v-html="post.title" />
    <span :date="post.date"/>
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
