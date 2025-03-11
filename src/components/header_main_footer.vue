<template>
    <div class="categories">
      <h2>Choisissez une catégorie :</h2>
      <ul>
        <li v-for="category in categories" :key="category.id">
          <button @click="selectCategory(category.id)">{{ category.name }}</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        categories: []
      };
    },
    created() {
      this.fetchCategories();
    },
    methods: {
      async fetchCategories() {
        try {
          const response = await fetch("https://api.example.com/categories");
          this.categories = await response.json();
        } catch (error) {
          console.error("Erreur de chargement des catégories", error);
        }
      },
      selectCategory(categoryId) {
        this.$router.push(`/quiz/${categoryId}`);
      }
    }
  };
  </script>
  
  <style scoped>
  .categories {
    text-align: center;
    margin: 20px;
  }
  .categories ul {
    list-style: none;
    padding: 0;
  }
  .categories button {
    background-color: #d9d9d9;
    border: none;
    padding: 10px;
    cursor: pointer;
  }
  </style>