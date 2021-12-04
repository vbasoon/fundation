<template>
  <form>
    <input v-model="title" class="input" type="text" placeholder="Title" />
    <input v-model="text" class="input" type="text" placeholder="Text" />
    <button @click="createPost">Add post</button>
  </form>
  <div class="post" v-for="post in posts">
    <div><strong>Title:</strong>{{ post.title }}</div>
    <div><strong>Text:</strong>{{ post.body }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { id: 1, title: "JavaScript", body: "Description1" },
        { id: 2, title: "React JS", body: "Description2" },
        { id: 3, title: "Vue JS", body: "Description3" },
        { id: 4, title: "OOP", body: "Description4" },
      ],
      title: "",
      text: "",
    };
  },
  methods() {
    this.posts.push();
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.post {
  font-size: 20px;
  margin-top: 30px;
  margin-left: 50px;
  width: 300px;
  height: 150px;
  border: 2px solid green;
}

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

button {
  margin-top: 20px;
  padding: 10px;
  background: none;
  border: 2px solid teal;
  font-size: 14px;
}

button:hover {
  background: teal;
  color: #fff;
  transition: color 0.5s ease-out;
}
</style>
