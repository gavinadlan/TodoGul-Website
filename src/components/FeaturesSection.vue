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
  height: auto; /* Hilangkan fixed height agar elemen bisa menyesuaikan */
  padding: 40px 20px; /* Kurangi padding di layar kecil */
  background-color: #f8f9ff;
  box-sizing: border-box;
  text-align: center;
}

.content {
  max-width: 1000px;
  margin: 0 auto;
}

h2 {
  font-size: 3rem; /* Tetap besar untuk tampilan utama */
  color: #8875ff; /* Tidak diubah, tetap warna ungu */
  margin-bottom: 20px;
  font-weight: bold;
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.description {
  font-size: 1rem; /* Ukuran lebih kecil agar lebih rapi */
  margin-bottom: 30px;
  line-height: 1.6; /* Line height lebih kecil untuk layar kecil */
}

.features-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 20px;
}

.feature-card {
  flex: 1 1 calc(33.333% - 20px); /* Tiga kolom untuk desktop */
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

/* Animations */
.fade-in.visible {
  opacity: 1;
  transform: translateY(0); /* Move to original position */
}

/* Responsiveness */
@media (max-width: 1024px) {
  .features-container {
    gap: 15px;
  }

  .feature-card {
    flex: 1 1 calc(50% - 15px); /* Dua kolom untuk tablet */
  }
}

@media (max-width: 768px) {
  h2 {
    font-size: 2rem; /* Hanya ukuran font yang berubah untuk ponsel */
  }

  .description {
    font-size: 0.9rem; /* Ukuran lebih kecil */
    line-height: 1.5; /* Jarak antar baris lebih kecil */
  }

  .features-container {
    gap: 10px; /* Kurangi jarak antar elemen */
  }

  .feature-card {
    flex: 1 1 100%; /* Satu kolom untuk ponsel */
    padding: 15px; /* Kurangi padding */
  }
}
</style>
