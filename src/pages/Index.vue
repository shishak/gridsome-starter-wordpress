<template>
  <Layout> 
    <div class="grid">
      <div class="box">
      <div class="grid-item" v-for="{ node } in $page.allWordPressPost.edges" :key="node.id"></div>
        <Post :post="node" />       
      </div>
    </div>
    <Pager :info="$page.allWordPressPost.pageInfo"/>
  </Layout>
</template>

<page-query>
query Home ($page: Int) {
  allWordPressPost (page: $page, perPage: 33) @paginate {
    pageInfo {
      totalPages
      currentPage
    }
    edges {
      node {
        id
        title
        path
        content
      }
    }
  }
}
</page-query>

<script>
import { Pager } from 'gridsome'
import Post from '~/components/Post.vue'

export default {
  components: {
    Pager,
    Post
  },
  metaInfo: {
    title: ''
  }
}
</script>
