<template>
  <section id="about">
    <div class="content">
      <h2 class="fade-in">About Us</h2>
      <p class="description fade-in">
        At Todogul, we are passionate about helping individuals and teams stay
        organized and efficient. We understand that managing tasks can often be
        overwhelming, which is why we've designed a solution that simplifies
        task management while enhancing productivity.
      </p>
      <p class="description fade-in">
        Our team is dedicated to creating intuitive, easy-to-use tools that make
        a difference. With Todogul, you can focus on what truly matters and
        leave the task management to us. Join the growing community of users who
        rely on Todogul to help them stay on top of their goals.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    // IntersectionObserver to trigger animations when the section comes into view
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
#about {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  padding: 40px;
  background-color: #f8f9ff; /* Light blue background */
  text-align: center;
  box-sizing: border-box;
}

.content {
  max-width: 800px; /* Limit the width of the content */
}

h2 {
  font-size: 3rem;
  color: #8875ff; /* Purple color */
  margin-bottom: 30px;
  font-weight: bold;
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.description {
  font-size: 1.25rem;
  color: #555; /* Soft gray color */
  line-height: 1.8;
  margin: 20px 0;
  font-weight: 400;
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0); /* Move to original position */
}
</style>
