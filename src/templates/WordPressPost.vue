<template>
  <Layout>
    <h1 v-html="$page.wordPressPost.title"/>
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
      
      
      <footer>
  <div class="footer-container">
    <section class="footer-main">
      <article>
       <h3>Learn</h3>
        <ul>
          <li><a href="#!">Guides</a></li>
          <li><a href="#!">Reference</a></li>
          <li><a href="#!">Samples</a></li>
          <li><a href="#!">Libraries</a></li>
          <li><a href="#!">Github</a></li>
        </ul>
      </article>
      <article>
        <h3>Learn</h3>
        <ul>
          <li><a href="#!">Guides</a></li>
          <li><a href="#!">Reference</a></li>
          <li><a href="#!">Samples</a></li>
          <li><a href="#!">Libraries</a></li>
          <li><a href="#!">Github</a></li>
        </ul>
      </article>
      <article>
        <h3>Stay connected</h3>
        <ul>
          <li><a href="#!">Blog</a></li>
          <li><a href="#!">Firebase Summit</a></li>
          <li><a href="#!">Facebook</a></li>
          <li><a href="#!">Twitter</a></li>
          <li><a href="#!">YouTube</a></li>
        </ul>
      </article>
      <article>
        <h3>Support</h3>
        <ul>
          <li><a href="#!">Contact support</a></li>
          <li><a href="#!">Stack Overflow</a></li>
          <li><a href="#!">Google Group</a></li>
          <li><a href="#!">Release notes</a></li>
          <li><a href="#!">FAQs</a></li>
          <li><a href="#!">Legacy documentation</a></li>
        </ul>
      </article>
    </section>
    <hr>
    <section class="footer-bottom">
      <small>© 2019 Google. All rights reserved.
      </small>
      <ul>
        <li><a href="#!">Facebook</a></li>
        <li><a href="#!">Twitter</a></li>
      </ul>
    </section>
  </div>
</footer>
  
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
export default {
  metaInfo () {
    return {
      title: this.$page.wordPressPost.title
    }
  }
}
</script>

<style>
 
</style>
