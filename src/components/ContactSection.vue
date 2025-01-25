<template>
  <section id="contact">
    <div class="content">
      <h2 class="fade-in">Contact Us</h2>
      <p class="description fade-in">
        We would love to hear from you! Please fill out the form below, and
        we'll get back to you as soon as possible.
      </p>
      <form>
        <input class="fade-in" type="text" placeholder="Your Name" required />
        <input class="fade-in" type="email" placeholder="Your Email" required />
        <textarea
          class="fade-in"
          placeholder="Your Message"
          required
        ></textarea>
        <button class="fade-in" type="submit">Send Message</button>
      </form>
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
#contact {
  padding: 80px 20px;
  background-color: #f8f9ff;
  text-align: center;
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
  color: #444;
  margin-bottom: 40px;
  line-height: 1.8;
  opacity: 0; /* Initially hidden */
  transform: translateY(50px); /* Start from below */
  transition: opacity 1s ease, transform 1s ease;
}

form {
  max-width: 600px;
  margin: 0 auto;
  background-color: white;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

input,
textarea {
  width: 100%;
  padding: 14px;
  margin: 12px 0;
  border: 1px solid #ccc;
  border-radius: 6px;
  font-size: 1rem;
}

input:focus,
textarea:focus {
  border-color: #8875ff;
  outline: none;
}

button {
  padding: 12px 24px;
  background-color: #8875ff;
  color: white;
  border: none;
  font-size: 1.25rem;
  cursor: pointer;
  border-radius: 8px;
  width: 100%;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #6653cc;
}

button:active {
  background-color: #5542a2;
}

/* Animation */
.fade-in.visible {
  opacity: 1;
  transform: translateY(0); /* Move to original position */
}
</style>
