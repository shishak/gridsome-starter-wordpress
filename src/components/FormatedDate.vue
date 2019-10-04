<template>
  <span>{{formatedDate}}</span>
</template>

<script>
import moment from "moment"
export default {
  props: {
    date: {
      type: String,
      required: true
    }
  },
  computed: {
    formatedDate() {
      return moment(this.date).locale('uk_UA').format('ll').fromNow();
    }
  }
}
</script>
