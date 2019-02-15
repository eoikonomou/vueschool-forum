<template>
  <span :title="seconds | humanFriendlyDate">{{seconds | diffForHumans}}</span>
</template>

<script>
import moment from 'moment'

export default {
  props: {
    seconds: {
      required: true,
      type: Number
    }
  },
  filters: {
    humanFriendlyDate(seconds) {
      return moment.unix(seconds).format('MMMM Do YYYY, h:mm:ss a')
    },
    diffForHumans(seconds) {
      return moment.unix(seconds).fromNow()
    }
  }
}
</script>
