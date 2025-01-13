<template>
  <section id="hero">
    <div class="hero-content">
      <h2>Building Innovative Solutions</h2>
      <p>
        Your partner in creating impactful solutions for your business needs.
      </p>
      <button>Get Started</button>
    </div>
  </section>
</template>

<style scoped>
#hero {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80vh;
  background-color: #f5f5f5;
  text-align: center;
}
.hero-content {
  max-width: 600px;
}
button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 4px;
}
button:hover {
  background-color: #0056b3;
}
</style>
