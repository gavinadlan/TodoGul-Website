<template>
  <section id="reviews">
    <div class="content">
      <h2 class="fade-in">Client Reviews</h2>
      <p class="description fade-in">
        Hear what our clients have to say about working with us. Our team is
        dedicated to delivering exceptional results!
      </p>
      <div class="reviews-container">
        <div class="review-card fade-in">
          <div class="reviewer-info">
            <img
              src="@/assets/samnod.png"
              alt="Reviewer 1"
              class="reviewer-photo"
            />
            <div>
              <cite>Donkey</cite>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
              </div>
            </div>
          </div>
          <p>
            "This company transformed our online presence and helped us grow our
            business! Highly recommend their services!"
          </p>
        </div>
        <div class="review-card fade-in">
          <div class="reviewer-info">
            <img
              src="@/assets/samnod.png"
              alt="Reviewer 2"
              class="reviewer-photo"
            />
            <div>
              <cite>Don Smith</cite>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="far fa-star"></i>
              </div>
            </div>
          </div>
          <p>
            "Professional team and excellent customer support. Our experience
            was fantastic!"
          </p>
        </div>
        <div class="review-card fade-in">
          <div class="reviewer-info">
            <img
              src="@/assets/samnod.png"
              alt="Reviewer 3"
              class="reviewer-photo"
            />
            <div>
              <cite>Naldi G Dragon</cite>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="far fa-star"></i>
              </div>
            </div>
          </div>
          <p>
            "Their attention to detail and dedication to quality made a huge
            impact on our business. Very pleased!"
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
#reviews {
  display: flex;
  align-items: center;
  justify-content: center;
  height: auto; /* Flex height for responsiveness */
  padding: 40px 20px; /* Padding for responsiveness */
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
  color: #8875ff; /* Keep the color as requested */
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

.reviews-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 20px;
}

.review-card {
  flex: 1 1 calc(33.333% - 20px);
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.review-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.review-card p {
  font-size: 1.125rem;
  color: #555;
  font-style: italic;
  margin-bottom: 10px;
}

.review-card cite {
  font-size: 1.125rem;
  font-weight: bold;
  color: #8875ff; /* Keep the color as requested */
}

.stars {
  color: gold;
  font-size: 1.5rem;
  margin-top: 5px;
}

.stars .fas {
  color: gold;
}

.stars .far {
  color: #ccc;
}

.reviewer-info {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}

.reviewer-photo {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 15px;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0); /* Move to original position */
}

/* Responsiveness */
@media (max-width: 768px) {
  .reviews-container {
    flex-direction: column; /* Stack cards vertically on smaller screens */
    align-items: center;
  }

  .review-card {
    flex: 1 1 100%; /* Full width cards */
    max-width: 90%; /* Slightly reduced max width */
    margin-bottom: 20px;
  }

  h2 {
    font-size: 2rem; /* Smaller heading on mobile */
  }

  .description {
    font-size: 1rem; /* Adjust description font size for smaller screens */
  }

  .stars {
    font-size: 1.25rem; /* Smaller star icons for mobile */
  }
}
</style>
