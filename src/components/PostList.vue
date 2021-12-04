<template>
  <div>
    <post-item
      class="post"
      v-for="post in posts"
      :key="post.id"
      :post="post"
    ></post-item>
  </div>
</template>

<script>
import PostItem from "./PostItem.vue";
export default {
  components: {
    PostItem,
  },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped></style>
