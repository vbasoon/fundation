<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {};
</script>

<style scoped>
.btn {
  margin-top: 20px;
  padding: 10px;
  background: none;
  border: 2px solid teal;
  font-size: 14px;
  transition: color 0.5s ease-out;
}

.btn:hover {
  background: teal;
  color: #fff;
  transition: color 0.5s ease-out;
  cursor: pointer;
}
</style>
