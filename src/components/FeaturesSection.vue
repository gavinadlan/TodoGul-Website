<template>
  <section id="features">
    <!-- Ubah id dari featureses menjadi features -->
    <div class="content">
      <h2 class="fade-in">APP FEATURES</h2>
      <p class="description fade-in">
        At Todogul, we focus on delivering a simple and efficient to-do list
        experience. Our services include designing sleek and user-friendly
        interfaces, integrating smooth animations, and ensuring that all
        interactions are seamless and intuitive. We are dedicated to making task
        management easier for you.
      </p>
      <div class="features-container">
        <div class="feature-card fade-in">
          <h3>Amazing UI Design</h3>
          <p>
            We design visually appealing and easy-to-navigate interfaces that
            make task management a breeze.
          </p>
        </div>
        <div class="feature-card fade-in">
          <h3>Soft And Smooth Animations</h3>
          <p>
            Experience smooth transitions and animations that make the app feel
            natural and responsive.
          </p>
        </div>
        <div class="feature-card fade-in">
          <h3>Friendly Interactions</h3>
          <p>
            Our goal is to create a user experience that is both intuitive and
            enjoyable, making task tracking effortless.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const elements = document.querySelectorAll(".fade-in");

    const observer = new IntersectionObserver(
      (entries, observer) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
          }
        });
      },
      { threshold: 0.5 }
    );

    elements.forEach((element) => {
      observer.observe(element);
    });
  },
};
</script>

<style scoped>
#features {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  padding: 40px;
  background-color: #f8f9ff;
  box-sizing: border-box;
  text-align: center;
}

.content {
  max-width: 1000px;
  margin: 0 auto;
}

h2 {
  font-size: 3rem;
  color: #8875ff;
  margin-bottom: 20px;
  font-weight: bold;
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.description {
  font-size: 1.25rem;
  color: #555;
  margin-bottom: 40px;
  line-height: 1.8;
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.features-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 20px;
}

.feature-card {
  flex: 1 1 calc(33.333% - 20px);
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.feature-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

h3 {
  font-size: 1.5rem;
  color: #8875ff;
  margin-top: 0;
}

.feature-card p {
  font-size: 1rem;
  color: #555;
  margin: 10px 0 0;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0); /* Move to original position */
}
</style>
