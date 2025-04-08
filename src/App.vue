<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import TodoInput from './components/TodoInput.vue';
import TodoFilter from './components/TodoFilter.vue';
import TodoList from './components/TodoList.vue';
</script>

<template>
  <div id="app" class="app-container">
    <Header />
    <div class="content-wrapper">
      <TodoInput />
      <TodoFilter />
      <TodoList />
    </div>
    <Footer />
  </div>
</template>


<style>
/* Modern CSS Reset and Base Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

html {
  font-size: 16px;
  line-height: 1.5;
}

html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  background: linear-gradient(135deg, #f5f7fa 0%, #e4e9f2 100%);
  font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  color: #1a202c;
  overflow-x: hidden;
}

#app {
  width: 100%;
  height: 100%;
  display: flex;
}

.app-container {
  width: 100%;
  min-height: 100vh;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  background: transparent;
  overflow-x: hidden;
}

.content-wrapper {
  flex: 1;
  display: flex;
  flex-direction: column;
  padding: clamp(1rem, 5vw, 2rem);
  overflow-y: auto;
  max-width: min(90%, 800px);
  width: 100%;
  margin: 0 auto;
  gap: 1.5rem;
  animation: fadeIn 0.3s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive Design */
@media (max-width: 768px) {
  html {
    font-size: 14px;
  }
  
  .content-wrapper {
    padding: 1rem;
  }
}

/* Custom Scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb {
  background: #cbd5e0;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #a0aec0;
}
</style>
