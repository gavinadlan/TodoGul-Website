<template>
  <section id="hero" class="hero">
    <div class="content">
      <h1 class="title">Welcome to Todogul</h1>
      <p class="subtitle">
        The best app to manage your tasks easily and efficiently.
      </p>
      <a
        href="https://github.com/gavinadlan/todogul.git"
        target="_blank"
        class="cta-button"
        >Download Now</a
      >
    </div>
    <div class="image-container">
      <img
        src="@/assets/Iphonetodogul.png"
        alt="iPhone dengan aplikasi Todogul"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: "HeroSection",
};
</script>

<style scoped>
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100vh;
  padding: 2rem;
  box-sizing: border-box;
  opacity: 0; /* Initial state hidden */
  animation: fadeIn 1s ease-out forwards;
}

.content {
  max-width: 50%;
  animation: slideInFromLeft 1s ease-out forwards;
}

.title {
  font-size: 3rem;
  color: #8875ff; /* Ungu */
  margin: 0;
}

.subtitle {
  font-size: 1.5rem;
  color: #444; /* Abu-abu gelap */
  margin: 1rem 0;
}

.cta-button {
  background-color: #8875ff;
  color: #fff;
  padding: 1rem 2rem;
  border: none;
  border-radius: 8px;
  font-size: 1.25rem;
  cursor: pointer;
  text-decoration: none; /* Remove underline */
  transition: background-color 0.3s ease;
}

.cta-button:hover {
  background-color: #6653cc; /* Warna ungu lebih gelap saat hover */
}

.image-container {
  max-width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  animation: slideInFromRight 1s ease-out forwards;
}

.image-container img {
  width: 120%;
  height: auto;
}

/* Keyframes for animations */
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideInFromLeft {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

@keyframes slideInFromRight {
  from {
    transform: translateX(100%);
  }
  to {
    transform: translateX(0);
  }
}
</style>
