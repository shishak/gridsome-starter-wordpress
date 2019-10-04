<template>
  <b-col lg="3" class="bg-light mt-4 mt-lg-5 p-4 rounded">
    <aside class="mb-5">
      <h2 class="mb-3 font-family-sans-serif h4">About</h2>
    </aside>
    <tags-widget class="mb-5"/>
    <categories-widget class="mb-5"/>
  </b-col>
</template>


<script>
import TagsWidget from '~/components/TagsWidget.vue'
import CategoriesWidget from '~/components/CategoriesWidget.vue'
export default {
  components: {
    TagsWidget,
    CategoriesWidget
  }
}
</script>
