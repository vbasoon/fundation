<template>
  <div class="post">
    <div class="post__title"><strong>Name: </strong>JavaScript</div>
    <hr />
    <div class="post__body"><strong>Text: </strong>Programm language</div>
  </div>
  <div class="post">
    <div class="post__title"><strong>Name: </strong>JavaScript</div>
    <hr />
    <div class="post__body"><strong>Text: </strong>Programm language</div>
  </div>
  <div class="post">
    <div class="post__title"><strong>Name: </strong>JavaScript</div>
    <hr />
    <div class="post__body"><strong>Text: </strong>Programm language</div>
  </div>
</template>

<script>
export default {
  data() {
    posts: [
      { id: 1, title: "JavaScript", body: "Description1" },
      { id: 2, title: "React JS", body: "Description2" },
      { id: 3, title: "Vue JS", body: "Description3" },
    ];
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
  margin-top: 50px;
  margin-left: 200px;
  width: 300px;
  height: 200px;
  border: 2px solid green;
}
</style>
