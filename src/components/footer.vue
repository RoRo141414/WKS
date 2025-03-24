<template>
  <footer class="footer" aria-label="Pied de page">
    <div class="footer-content">
      Blind Test Musical - 2025
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: #1a1a1a;
  color: white;
  border-top: 2px solid white;
}

.footer-content {
  font-size: 1rem;
  text-align: center;
}
</style>