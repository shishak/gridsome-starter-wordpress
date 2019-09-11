<template>
  <div>
   <g-link :to="post.path">
    <h2 v-html="post.title" />
     </g-link>
    <g-image :src="$page.post.image" />
  </div>
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
