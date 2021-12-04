<template>
  <div class="post">
    <div>
      <div><strong>Title:</strong>{{ post.title }}</div>
      <div><strong>Text:</strong>{{ post.text }}</div>
    </div>
    <div class="post__btns">
      <my-button>Del</my-button>
    </div>
  </div>
</template>

<script>
import MyButton from "./UI/MyButton.vue";
export default {
  components: { MyButton },
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
.post {
  display: flex;
  justify-content: space-between;
  padding: 10px;
  font-size: 20px;
  margin-top: 30px;
  margin-left: 50px;
  width: 300px;
  height: 150px;
  border: 2px solid green;
}

my-button:hover {
  background: teal;
  color: #fff;
  transition: color 0.5s ease-out;
}
</style>
