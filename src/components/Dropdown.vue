<template>
    <select @change="handleChange" class="custom-dropdown">
      <option v-for="option in options" :key="option.value" :value="option.value">{{ option.label }}</option>
    </select>
  </template>
  
  <script>
  export default {
    name: "CustomDropdown",
    props: {
      options: {
        type: Array,
        required: true
      }
    },
    methods: {
      handleChange(event) {
        this.$emit("change", event.target.value);
      }
    }
  };
  </script>
  
  <style scoped>
  .custom-dropdown {
    padding: 8px;
    border: 1px solid #ccc;
  }
  </style>
  