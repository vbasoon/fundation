<template>
  <form @submit.prevent>
    <my-input v-model="post.title" type="text" placeholder="Title" />
    <my-input v-model="post.text" type="text" placeholder="Text" />
    <my-button @click="createPost">Add post</my-button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        text: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        text: "",
      };
    },
  },
};
</script>

<style scoped>
form {
  max-width: 600px;
  margin-left: 50px;
}
</style>
