<template>
  <header class="header">
    <h1 class="app-title">Nuxt Todo App</h1>
    <button class="share-button">
      <span class="share-icon">⤴</span>
    </button>
  </header>
</template>

<script setup>
// Header component using script setup syntax
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0;
  padding: clamp(1rem, 3vw, 1.5rem);
  background: linear-gradient(to right, #2c5364, #203a43, #0f2027);
  color: white;
  width: 100%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.app-title {
  margin: 0;
  font-size: clamp(1.5rem, 4vw, 1.75rem);
  font-weight: 700;
  color: white;
  letter-spacing: -0.5px;
  background: linear-gradient(120deg, #ffffff, #e2e8f0);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.share-button {
  background: linear-gradient(135deg, #4299e1, #3182ce);
  border: none;
  color: white;
  font-size: 1rem;
  cursor: pointer;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.share-button:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  background: linear-gradient(135deg, #3182ce, #2c5282);
}

.share-icon {
  transform: rotate(45deg);
  display: inline-block;
  font-weight: bold;
}

@media (max-width: 768px) {
  .header {
    padding: 1rem;
  }
  
  .share-button {
    padding: 0.4rem 0.8rem;
  }
}
</style>