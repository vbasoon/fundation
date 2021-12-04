<template>
  <input
    :value="modelValue"
    @input="updateInput"
    class="input"
    type="text"
    name=""
    id=""
  />
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
.input {
  width: 100%;
  border: 2 solid blue;
  padding: 10px;
  margin-top: 10px;
  font-size: 14px;
}

.input:hover {
  border: 2px solid teal;
}
</style>
