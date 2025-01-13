<template>
  <section id="contact">
    <h2>Contact Us</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>
</template>

<style scoped>
#contact {
  padding: 60px 20px;
  background-color: #f5f5f5;
  text-align: center;
}
h2 {
  font-size: 32px;
  margin-bottom: 40px;
}
form {
  max-width: 500px;
  margin: 0 auto;
}
input,
textarea {
  width: 100%;
  padding: 12px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 4px;
}
button {
  padding: 12px 24px;
  background-color: #007bff;
  color: white;
  border: none;
  font-size: 16px;
  cursor: pointer;
  border-radius: 4px;
}
button:hover {
  background-color: #0056b3;
}
</style>
