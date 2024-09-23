<template>
    <input type="range" :min="min" :max="max" v-model="value" @input="handleInput" />
  </template>
  
  <script>
  export default {
    name: "CustomSlider",
    props: {
      min: {
        type: Number,
        default: 0
      },
      max: {
        type: Number,
        default: 100
      },
      value: {
        type: Number,
        default: 50
      }
    },
    methods: {
      handleInput(event) {
        this.$emit("input", event.target.value);
      }
    }
  };
  </script>
  