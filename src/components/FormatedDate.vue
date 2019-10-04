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
      return moment(this.date).fromNow();
    }
  }
}


moment.updateLocale('en', {
    relativeTime : {
        past: function(input) {
          return input === 'just now'
            ? input
            : input + ' ago'
        },
        s  : 'just now',
        future: "in %s",
        ss : '%d seconds',
        m:  "a minute",
        mm: "%d minutes",
        h:  "an hour",
        hh: "%d hours",
        d:  "a day",
        dd: "%d days",
        M:  "a month",
        MM: "%d months",
        y:  "a year",
        yy: "%d years"
    }
});
</script>
