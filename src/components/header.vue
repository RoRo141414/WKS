<template>
  <header class="header">
    <h1 class="title">Blind Test</h1>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 15px 30px;
  background: linear-gradient(135deg, #1e3c72, #2a5298);
  color: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.title {
  font-size: 1.8rem;
  margin: 0;
  text-align: center;
}
</style>