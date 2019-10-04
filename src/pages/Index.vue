<template>
  <Layout> 
  <div class="container">
    <div class="grid">
      <div class="col box" v-for="{ node } in $page.allWordPressPost.edges" :key="node.id">
        <Post :post="node" />
      </div>
    </div>
   </div> 
    <Pager :info="$page.allWordPressPost.pageInfo"/>
  </Layout>
</template>

<page-query>
query Home ($page: Int) {
  allWordPressPost (page: $page, perPage: 10) @paginate {
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
