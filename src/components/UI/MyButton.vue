<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {};
</script>

<style scoped>
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
