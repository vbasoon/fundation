<template>
  <div class="post" v-for="post in posts">
    <div><strong>Title:</strong>{{ post.title }}</div>
    <div><strong>Text:</strong>{{ post.text }}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.post {
  font-size: 20px;
  margin-top: 30px;
  margin-left: 50px;
  width: 300px;
  height: 150px;
  border: 2px solid green;
}
</style>
