<template>
  <form @submit.prevent>
    <input v-model="post.title" class="input" type="text" placeholder="Title" />
    <input v-model="post.text" class="input" type="text" placeholder="Text" />
    <my-button @click="createPost">Add post</my-button>
  </form>
</template>

<script>
import MyButton from "./UI/MyButton.vue";
export default {
  components: { MyButton },
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

.input {
  width: 100%;
  border: 2 solid blue;
}

input {
  padding: 10px;
  margin-top: 10px;
  font-size: 14px;
}

input:hover {
  border: 2px solid teal;
}
</style>
