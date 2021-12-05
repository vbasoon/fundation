<template>
  <post-form @create="createPost" />
  <post-list :posts="posts" @remove="removePost" />
</template>

<script>
import PostForm from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";

export default {
  components: {
    PostForm,
    PostList,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "JavaScript", text: "Description1" },
        { id: 2, title: "React JS", text: "Description2" },
        { id: 3, title: "Vue JS", text: "Description3" },
        { id: 4, title: "OOP", text: "Description4" },
      ],
    };
  },
  methods: {
    createPost(post) {
      this.posts = [post, ...this.posts];
    },
    removePost(post) {
      this.posts = this.posts.filter((p) => p.id !== post.id);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  padding: 20px;
}
</style>
