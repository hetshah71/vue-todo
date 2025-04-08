<template>
  <footer class="footer">
    <nav class="footer-nav">
      <a href="#" class="nav-link home-link">Home</a>
      <a href="#" class="nav-link about-link">About</a>
      <a href="#" class="nav-link contact-link">Contact</a>
    </nav>
  </footer>
</template>

<script setup>
// Footer component using script setup syntax
</script>

<style scoped>
.footer {
  margin-top: auto;
  background: linear-gradient(to right, #2c5364, #203a43, #0f2027);
  padding: clamp(0.8rem, 2vw, 1.2rem);
  width: 100%;
  box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.1);
}

.footer-nav {
  display: flex;
  justify-content: center;
  gap: clamp(1.5rem, 4vw, 2.5rem);
  max-width: min(90%, 800px);
  margin: 0 auto;
}

.nav-link {
  color: #e2e8f0;
  text-decoration: none;
  font-size: clamp(0.8rem, 2vw, 0.875rem);
  transition: all 0.3s ease;
  padding: 0.5rem 0.8rem;
  border-radius: 4px;
  position: relative;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, #4299e1, #3182ce);
  transition: all 0.3s ease;
  transform: translateX(-50%);
}

.nav-link:hover {
  color: #ffffff;
}

.nav-link:hover::after {
  width: 100%;
}

@media (max-width: 768px) {
  .footer-nav {
    gap: 1rem;
  }
  
  .nav-link {
    padding: 0.4rem 0.6rem;
  }
}
</style>