<template>
  <div class="post-list">
    <PostListItem :key="post['.key']" v-for="post in posts" :post="post"/>
  </div>
</template>

<script>
import sourceData from '@/data'
import PostListItem from './PostListItem'

export default {
  props: {
    posts: {
      required: true,
      type: Array
    }
  },
  components: {
    PostListItem
  }
}
</script>
