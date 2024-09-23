<template>
    <div class="grid">
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    name: "CustomGrid"
  };
  </script>
  
  <style scoped>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
  }
  </style>
  