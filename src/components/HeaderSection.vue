<template>
  <header>
    <div class="logo">
      <h1>TODOGUL</h1>
    </div>
    <nav>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#testimonials">Testimonials</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background-color: #333;
  color: white;
}
.logo h1 {
  margin: 0;
}
nav a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
}
nav a:hover {
  text-decoration: underline;
}
</style>
