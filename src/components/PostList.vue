<template>
  <div v-show="posts.length > 0">
    <h3>Список постов</h3>
    <post-item
      class="post"
      v-for="post in posts"
      :post="post"
      :key="post.id"
      @remove="$emit('remove', post)"
    />
  </div>
  <div v-show="posts.length === 0">
    <h3 style="color: red; margin-left: 50px">Список постів пустий</h3>
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
