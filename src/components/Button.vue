<template>
    <button :disabled="loading" @click="handleClick" class="custom-button">
      <span v-if="!loading">{{ label }}</span>
      <span v-else>
        <svg class="spinner" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
          <circle class="path" fill="none" stroke-width="8" stroke-linecap="round" cx="50" cy="50" r="35"></circle>
        </svg>
      </span>
    </button>
  </template>
  
  <script>
  export default {
    name: "CustomButton",
    props: {
      label: {
        type: String,
        default: "Click Me"
      },
      loading: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      handleClick() {
        this.$emit("myclick");
      }
    }
  };
  </script>
  
  <style scoped>
  .custom-button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
    display: inline-flex;
    justify-content: center;
    align-items: center;
  }
  
  .spinner {
    animation: rotate 1s linear infinite;
    width: 20px;
    height: 20px;
  }
  
  .path {
    stroke: white;
    stroke-dasharray: 90, 150;
    stroke-dashoffset: 0;
    transform-origin: center;
    animation: dash 1.5s ease-in-out infinite;
  }
  </style>
  