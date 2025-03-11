<template>
    <div class="title-container">
      <h1>{{ songTitle }}</h1>
      <p>{{ artistName }}</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from "vue";
  
  defineProps({
    songTitle: String,
    artistName: String
  });
  </script>
  
  <style scoped>
  .title-container {
    text-align: center;
    margin: 20px 0;
  }
  
  h1 {
    font-size: 24px;
  }
  
  p {
    font-size: 18px;
    color: gray;
  }
  </style>