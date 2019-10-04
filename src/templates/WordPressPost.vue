<template>
  <Layout>
    <h1 v-html="$page.wordPressPost.title"/>
    <formated-date class="post-date" :date="post.date"/>
    <div v-html="$page.wordPressPost.content"/>
    <template v-if="$page.wordPressPost.categories.length">
      <h4>Posted in</h4>
      <ul class="list categories">
        <li v-for="category in $page.wordPressPost.categories" :key="category.id" >
          <g-link :to="category.path">{{ category.title }}</g-link>
        </li>
      </ul>
    </template>
    <template v-if="$page.wordPressPost.tags.length">
      <h4>Tags</h4>
      <ul class="list tags">
        <li v-for="tag in $page.wordPressPost.tags" :key="tag.id" >
          <g-link :to="tag.path">{{ tag.title }}</g-link>
        </li>
      </ul>
    </template>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
  wordPressPost (path: $path) {
    title
    content
    categories {
      id
      title
      path
    }
    tags {
      id
      title
      path
    }
  }
}
</page-query>

<script>
import FormatedDate from "~/components/FormatedDate.vue"

export default {
  FormatedDate,
  metaInfo () {
    return {
      title: this.$page.wordPressPost.title
    }
  }
}
</script>

<style>
 
</style>
