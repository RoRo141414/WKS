<template>
    <div class="categories">
      <h2>Choisissez une catégorie</h2>
      <div v-if="loading">Chargement...</div>
      <ul v-else>
        <li v-for="category in categories" :key="category.id">
          <button @click="selectCategory(category.id)">{{ category.name }}</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from "vue";
  
  const categories = ref([]);
  const loading = ref(true);
  
  const fetchCategories = async () => {
    try {
      const response = await fetch("https://api.example.com/categories"); // Remplace par ton API
      categories.value = await response.json();
    } catch (error) {
      console.error("Erreur lors de la récupération des catégories", error);
    } finally {
      loading.value = false;
    }
  };
  
  const selectCategory = (categoryId) => {
    console.log("Catégorie sélectionnée:", categoryId);
    // Rediriger vers le quiz de cette catégorie
  };
  
  onMounted(fetchCategories);
  </script>
  
  <style scoped>
  .categories {
    text-align: center;
  }
  
  ul {
    list-style: none;
    padding: 0;
  }
  
  li {
    margin: 10px 0;
  }
  
  button {
    padding: 10px;
    background-color: #d9d9d9;
    border: none;
    cursor: pointer;
  }
  </style>