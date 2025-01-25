<template>
  <header>
    <div class="logo">
      <a href="#hero">
        <h1>TODOGUL</h1>
      </a>
    </div>
    <nav>
      <a href="#about">About</a>
      <a href="#features">Features</a>
      <a href="#reviews">Reviews</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px;
  background-color: #8875ff;
  color: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo a {
  text-decoration: none; /* Menghilangkan underline di link */
}

.logo h1 {
  margin: 0;
  font-size: 1.75rem;
  font-weight: bold;
  letter-spacing: 2px;
  color: white;
}

nav a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
  font-size: 1rem;
  font-weight: 500;
  transition: color 0.3s ease;
}

nav a:hover {
  color: #f8f9ff;
}

nav a:active {
  color: #ddd;
}
</style>
