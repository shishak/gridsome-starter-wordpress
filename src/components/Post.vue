<template>
   <g-link :to="post.path" class="grid-item">
    <div v-html="post.content" />
    <h2 v-html="post.title" />
    <formated-date class="post-date font-weight-bold" :date="post.date"/>
   </g-link>     
</template>

<script>
import FormatedDate from "~/components/FormatedDate.vue"
export default {
  components: {
    FormatedDate
  },
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>
